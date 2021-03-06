---
title: '방법: 서비스 모니커 등록 및 구성'
ms.date: 03/30/2017
helpviewer_keywords:
- COM [WCF], configure service monikers
- COM [WCF], register service monikers
ms.assetid: e5e16c80-8a8e-4eef-af53-564933b651ef
ms.openlocfilehash: cd3b6bbb47dfd72bf70091c9ca4d6fc5e228d950
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44221547"
---
# <a name="how-to-register-and-configure-a-service-moniker"></a>방법: 서비스 모니커 등록 및 구성
형식화 된 계약을 사용 하 여 COM 응용 프로그램 내에서 Windows Communication Foundation (WCF) 서비스 모니커를 사용 하기 전에 필수 특성 사용된 형식이 COM에 등록 하며 필요한 바인딩을 사용 하 여 COM 응용 프로그램과 모니커를 구성 합니다. 구성입니다.  
  
### <a name="to-register-the-required-attributed-types-with-com"></a>필요한 특성을 사용하는 형식을 COM에 등록하려면  
  
1.  사용 된 [ServiceModel Metadata 유틸리티 도구 (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) WCF 서비스에서 메타 데이터 계약을 검색 하는 도구입니다. 이 WCF 클라이언트 어셈블리 및 클라이언트 응용 프로그램 구성 파일에 대 한 소스 코드를 생성합니다.  
  
2.  어셈블리의 형식이 `ComVisible`로 표시되는지 확인합니다. 이렇게 하려면 Visual Studio 프로젝트의 AssemblyInfo.cs 파일에 다음 특성을 추가합니다.  
  
    ```  
    [assembly: ComVisible(true)]  
    ```  
  
3.  관리 되는 WCF 클라이언트를 강력한 이름의 어셈블리로 컴파일하십시오. 이렇게 하려면 암호화된 키 쌍으로 서명해야 합니다. 자세한 내용은 [강력한 이름으로 어셈블리 서명](https://go.microsoft.com/fwlink/?LinkId=94874) .NET Developer's Guide에 있습니다.  
  
4.  어셈블리 등록(Regasm.exe) 도구에 `/tlb` 옵션을 사용하여 어셈블리의 형식을 COM에 등록합니다.  
  
5.  전역 어셈블리 캐시(Gacutil.exe) 도구를 사용하여 어셈블리를 전역 어셈블리 캐시에 추가합니다.  
  
    > [!NOTE]
    >  어셈블리에 서명하고 전역 어셈블리 캐시에 추가하는 것은 선택적 단계이지만 런타임에 올바른 위치에서 어셈블리를 로드하는 프로세스를 단순화할 수 있습니다.  
  
### <a name="to-configure-the-com-application-and-the-moniker-with-the-required-binding-configuration"></a>필요한 바인딩 구성을 사용하여 COM 응용 프로그램과 모니커를 구성하려면  
  
-   바인딩 정의 배치 (에서 생성 합니다 [ServiceModel Metadata 유틸리티 도구 (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) 생성 된 클라이언트 응용 프로그램 구성 파일에서) 클라이언트 응용 프로그램의 구성 파일. 예를 들어 이름이 CallCenterClient.exe인 Visual Basic 6.0 실행 파일에 대해 실행 파일과 동일한 디렉터리 내의 CallCenterConfig.exe.config 파일에 구성을 저장해야 합니다. 이제 클라이언트 응용 프로그램에서 모니커를 사용할 수 있습니다. 참고는 표준 바인딩 WCF에서 제공 하는 형식 중 하나를 사용 하는 경우 바인딩 구성이 필요 하지 않습니다.  
  
     다음 형식이 등록됩니다.  
  
    ```  
    using System.ServiceModel;  
  
    ...  
  
    [ServiceContract]   
    public interface IMathService   
    {  
    [OperationContract]  
    public int Add(int x, int y);  
    [OperationContract]  
    public int Subtract(int x, int y);  
    }  
    ```  
  
     응용 프로그램은 `wsHttpBinding` 바인딩을 사용하여 노출됩니다. 지정된 형식과 응용 프로그램 구성에 대해 다음 예제 모니커 문자열이 사용됩니다.  
  
    ```  
    service4:address=http://localhost/MathService, binding=wsHttpBinding, bindingConfiguration=Binding1  
    ```  
  
     `or`  
  
    ```  
    service4:address=http://localhost/MathService, binding=wsHttpBinding, bindingConfiguration=Binding1, contract={36ADAD5A-A944-4d5c-9B7C-967E4F00A090}  
    ```  
  
     다음 샘플 코드와 같이 `IMathService` 형식을 포함하는 어셈블리에 대한 참조를 추가한 후 Visual Basic 6.0 응용 프로그램 내에서 이러한 모니커 문자열 중 하나를 사용할 수 있습니다.  
  
    ```  
    Dim MathProxy As IMathService  
    Dim result As Integer  
  
    Set MathProxy = GetObject( _  
            "service4:address=http://localhost/MathService, _  
            binding=wsHttpBinding, _  
            bindingConfiguration=Binding1")  
  
    result = MathProxy.Add(3, 5)  
    ```  
  
     이 예제에서 바인딩 구성 `Binding1`의 정의는 클라이언트 응용 프로그램에 대한 적절한 이름의 구성 파일(예: vb6appname.exe.config)에 저장됩니다.  
  
    > [!NOTE]
    >  C#, C++ 또는 다른 모든 .NET 언어 응용 프로그램으로 유사한 코드를 사용할 수 있습니다.  
  
    > [!NOTE]
    >  모니커가 잘못 작동하거나 서비스를 사용할 수 없는 경우 `GetObject`를 호출하면 "구문이 잘못되었습니다"라는 오류가 반환됩니다. 이 오류가 발생하면 사용하고 있는 모니커가 올바르고 서비스를 사용할 수 있는지 확인하세요.  
  
     이 항목에서는 VB 6.0 코드의 서비스 모니커 사용에 중점을 두지만 다른 언어에서 서비스 모니커를 사용할 수 있습니다. C++ 코드에서 모니커를 사용하는 경우 다음 코드와 같이 "no_namespace named_guids raw_interfaces_only"를 사용하여 Svcutil.exe에서 생성된 어셈블리를  가져와야 합니다.  
  
    ```  
    #import "ComTestProxy.tlb" no_namespace named_guids  
    ```  
  
     모든 메서드에서 `HResult`를 반환하도록 가져온 인터페이스 정의를 수정합니다. 다른 모든 반환 값은 출력 매개 변수로 변환됩니다. 전체 메서드 실행은 동일하게 유지됩니다. 이 경우 프록시에서 메서드를 호출할 때 예외의 원인을 확인할 수 있습니다. 이 기능은 C++ 코드에서만 사용할 수 있습니다.  
  
## <a name="see-also"></a>참고 항목  
 [ServiceModel Metadata 유틸리티 도구(Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)
