---
title: ICorDebugRemote 인터페이스
ms.date: 03/30/2017
api_name:
- ICorDebugRemote
api_location:
- CorDebug.dll
api_type:
- COM
f1_keywords:
- ICorDebugRemote
helpviewer_keywords:
- ICorDebugRemote interface [.NET Framework debugging]
ms.assetid: 53d073c6-fa02-40d2-82e1-b9452bb6abaa
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ab8ed5c4fa3dc0ed77c1948aa6c1b940ecc25c14
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33421453"
---
# <a name="icordebugremote-interface"></a>ICorDebugRemote 인터페이스
시작할 수 있거나 원격 대상 프로세스에 관리되는 디버거를 연결할 수 있는 기능을 제공합니다.  
  
## <a name="syntax"></a>구문  
  
```  
interface ICorDebugRemote : IUnknown  
{  
    HRESULT CreateProcessEx  
      (  
      [in] ICorDebugRemoteTarget *     pRemoteTarget,  
      [in] LPCWSTR                     lpApplicationName,  
      [in] LPWSTR                      lpCommandLine,  
      [in] LPSECURITY_ATTRIBUTES       lpProcessAttributes,  
      [in] LPSECURITY_ATTRIBUTES       lpThreadAttributes,  
      [in] BOOL                        bInheritHandles,  
      [in] DWORD                       dwCreationFlags,  
      [in] PVOID                       lpEnvironment,  
      [in] LPCWSTR                     lpCurrentDirectory,  
      [in] LPSTARTUPINFOW              lpStartupInfo,  
      [in] LPPROCESS_INFORMATION       lpProcessInformation,  
      [in] CorDebugCreateProcessFlags  debuggingFlags,  
      [out] ICorDebugProcess **        ppProcess  
      );  
  
    HRESULT DebugActiveProcessEx  
      (  
      [in] ICorDebugRemoteTarget *   pRemoteTarget,  
      [in] DWORD                     dwProcessId,  
      [in] BOOL                      fWin32Attach,  
      [out] ICorDebugProcess **      ppProcess  
      );  
};  
```  
  
## <a name="methods"></a>메서드  
  
|메서드|설명|  
|------------|-----------------|  
|[ICorDebugRemote::CreateProcessEx 메서드](../../../../docs/framework/unmanaged-api/debugging/icordebugremote-createprocessex-method.md)|관리 되는 디버깅에 대 한 원격 컴퓨터에서 프로세스를 만듭니다.|  
|[ICorDebugRemote::DebugActiveProcessEx 메서드](../../../../docs/framework/unmanaged-api/debugging/icordebugremote-debugactiveprocessex-method.md)|디버거에서 원격 컴퓨터에서 프로세스를 시작합니다.|  
  
## <a name="remarks"></a>설명  
 현재이 기능은 원격 Macintosh 컴퓨터에서 실행 되는 Silverlight 기반 응용 프로그램 대상 디버깅에 대해서만 지원 됩니다.  
  
## <a name="requirements"></a>요구 사항  
 **플랫폼:** 참조 [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)합니다.  
  
 **헤더:** CorDebug.idl, CorDebug.h  
  
 **라이브러리:** CorGuids.lib  
  
 **.NET framework 버전:** 4.5, 4, 3.5 SP1  
  
## <a name="see-also"></a>참고 항목  
 [ICorDebugRemoteTarget 인터페이스](../../../../docs/framework/unmanaged-api/debugging/icordebugremotetarget-interface.md)  
 [ICorDebug 인터페이스](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md)  
    
 [디버깅 인터페이스](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
