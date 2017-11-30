---
title: "ICorDebugController::Detach 메서드"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugController.Detach
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugController::Detach
helpviewer_keywords:
- Detach method, ICorDebugController interface [.NET Framework debugging]
- ICorDebugController::Detach method [.NET Framework debugging]
ms.assetid: 06fae364-f2c6-4a50-aa7e-3da9f2684dc3
topic_type: apiref
caps.latest.revision: "11"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 2d8c1df2fd2aa52f9f5e90a27d42f6568686e908
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugcontrollerdetach-method"></a><span data-ttu-id="3b1a5-102">ICorDebugController::Detach 메서드</span><span class="sxs-lookup"><span data-stu-id="3b1a5-102">ICorDebugController::Detach Method</span></span>
<span data-ttu-id="3b1a5-103">프로세스 또는 응용 프로그램 도메인에서 디버거를 분리 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-103">Detaches the debugger from the process or application domain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3b1a5-104">구문</span><span class="sxs-lookup"><span data-stu-id="3b1a5-104">Syntax</span></span>  
  
```  
HRESULT Detach ();  
```  
  
## <a name="remarks"></a><span data-ttu-id="3b1a5-105">설명</span><span class="sxs-lookup"><span data-stu-id="3b1a5-105">Remarks</span></span>  
 <span data-ttu-id="3b1a5-106">프로세스 또는 응용 프로그램 도메인을 정상적으로 실행을 계속 하지만 "ICorDebugProcess" 또는 "ICorDebugAppDomain" 개체를 더 이상 사용할 하 고 더 이상 없는 콜백이 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-106">The process or application domain continues execution normally, but the "ICorDebugProcess" or "ICorDebugAppDomain" object is no longer valid and no further callbacks will occur.</span></span>  
  
 <span data-ttu-id="3b1a5-107">.NET Framework 버전 2.0에서에서 관리 되지 않는 디버깅을 설정한 경우 운영 체제 제한으로 인해이 메서드가 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-107">In the .NET Framework version 2.0, if unmanaged debugging is enabled, this method will fail due to operating system limitations.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3b1a5-108">요구 사항</span><span class="sxs-lookup"><span data-stu-id="3b1a5-108">Requirements</span></span>  
 <span data-ttu-id="3b1a5-109">**플랫폼:** 참조 [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3b1a5-110">**헤더:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3b1a5-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3b1a5-111">**라이브러리:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3b1a5-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3b1a5-112">**.NET framework 버전:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3b1a5-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3b1a5-113">참고 항목</span><span class="sxs-lookup"><span data-stu-id="3b1a5-113">See Also</span></span>  
 