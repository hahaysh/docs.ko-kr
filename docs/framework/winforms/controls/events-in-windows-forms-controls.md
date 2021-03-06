---
title: Windows Forms 컨트롤의 이벤트
ms.date: 03/30/2017
helpviewer_keywords:
- events [Windows Forms], custom controls (using code)
- custom controls [Windows Forms], events overview (using code)
ms.assetid: 7e3d1379-87aa-437c-afce-c99454eff30e
ms.openlocfilehash: d18938565c302be085b7ac51f878d83ae5ab533d
ms.sourcegitcommit: 69229651598b427c550223d3c58aba82e47b3f82
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/04/2018
ms.locfileid: "48584054"
---
# <a name="events-in-windows-forms-controls"></a>Windows Forms 컨트롤의 이벤트
Windows Forms 컨트롤에서 60 개 이상의 이벤트를 상속 <xref:System.Windows.Forms.Control?displayProperty=nameWithType>합니다. 여기에 포함 됩니다는 <xref:System.Windows.Forms.Control.Paint> 컨트롤을 그릴 수 있도록 하는 이벤트와 같은 창을 표시와 관련 된 이벤트를 <xref:System.Windows.Forms.Control.Resize> 및 <xref:System.Windows.Forms.Control.Layout> 이벤트 및 낮은 수준의 마우스 및 키보드 이벤트입니다. 일부 하위 수준 이벤트에서 합성 됩니다 <xref:System.Windows.Forms.Control> 와 같은 의미 체계 이벤트에 <xref:System.Windows.Forms.Control.Click> 고 <xref:System.Windows.Forms.Control.DoubleClick>입니다. 상속 된 이벤트에 대 한 세부 정보를 참조 하세요. <xref:System.Windows.Forms.Control>합니다.  
  
 사용자 지정 컨트롤이 상속된 이벤트 기능을 재정의해야 하는 경우 대리자를 연결하는 대신 상속된 `On`*EventName* 메서드를 재정의합니다. .NET Framework에서 이벤트 모델에 익숙하지 않다면 [구성 요소에서 이벤트 발생 시키기](https://msdn.microsoft.com/library/9aebf605-a87d-470b-b7c8-f9abfc8360a0)를 참조하세요.  
  
## <a name="see-also"></a>참고 항목  
 [OnPaint 메서드 재정의](../../../../docs/framework/winforms/controls/overriding-the-onpaint-method.md)  
 [사용자 입력 처리](../../../../docs/framework/winforms/controls/handling-user-input.md)  
 [이벤트 정의](../../../../docs/framework/winforms/controls/defining-an-event-in-windows-forms-controls.md)  
 [이벤트](../../../../docs/standard/events/index.md)
