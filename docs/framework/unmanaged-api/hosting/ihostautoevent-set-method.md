---
title: "IHostAutoEvent::Set 메서드"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IHostAutoEvent.Set
api_location: mscoree.dll
api_type: COM
f1_keywords: IHostAutoEvent::Set
helpviewer_keywords:
- Set method, IHostAutoEvent interface [.NET Framework hosting]
- IHostAutoEvent::Set method [.NET Framework hosting]
ms.assetid: 46becf3e-bc0e-4338-85c0-9ab0df76a1d0
topic_type: apiref
caps.latest.revision: "12"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 07de2321c1c7760293c53ad77dd3bbdf7f82a564
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/21/2017
---
# <a name="ihostautoeventset-method"></a><span data-ttu-id="e413f-102">IHostAutoEvent::Set 메서드</span><span class="sxs-lookup"><span data-stu-id="e413f-102">IHostAutoEvent::Set Method</span></span>
<span data-ttu-id="e413f-103">에서는 현재 [IHostAutoEvent](../../../../docs/framework/unmanaged-api/hosting/ihostautoevent-interface.md) 인스턴스 신호를 받은 상태로 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e413f-103">Sets the current [IHostAutoEvent](../../../../docs/framework/unmanaged-api/hosting/ihostautoevent-interface.md) instance to a signaled state.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e413f-104">구문</span><span class="sxs-lookup"><span data-stu-id="e413f-104">Syntax</span></span>  
  
```  
HRESULT Set ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="e413f-105">반환 값</span><span class="sxs-lookup"><span data-stu-id="e413f-105">Return Value</span></span>  
  
|<span data-ttu-id="e413f-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="e413f-106">HRESULT</span></span>|<span data-ttu-id="e413f-107">설명</span><span class="sxs-lookup"><span data-stu-id="e413f-107">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="e413f-108">S_OK</span><span class="sxs-lookup"><span data-stu-id="e413f-108">S_OK</span></span>|<span data-ttu-id="e413f-109">`Set`성공적으로 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e413f-109">`Set` returned successfully.</span></span>|  
|<span data-ttu-id="e413f-110">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="e413f-110">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="e413f-111">공용 언어 런타임 (CLR) 프로세스에 로드 되지 않았습니다 또는 CLR 중인 상태를 관리 코드를 실행 하거나 호출을 처리할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e413f-111">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="e413f-112">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="e413f-112">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="e413f-113">호출 시간이 초과 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e413f-113">The call timed out.</span></span>|  
|<span data-ttu-id="e413f-114">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="e413f-114">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="e413f-115">호출자에 게 잠금을 소유 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e413f-115">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="e413f-116">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="e413f-116">HOST_E_ABANDONED</span></span>|<span data-ttu-id="e413f-117">차단 된 스레드 이벤트 취소 되었습니다 또는 파이버가 기다리던 합니다.</span><span class="sxs-lookup"><span data-stu-id="e413f-117">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="e413f-118">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="e413f-118">E_FAIL</span></span>|<span data-ttu-id="e413f-119">알 수 없는 치명적인 오류가 발생 했습니다.</span><span class="sxs-lookup"><span data-stu-id="e413f-119">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="e413f-120">메서드가 E_FAIL을 반환 하는 경우 CLR을 하는 프로세스 내에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e413f-120">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="e413f-121">호스팅 방법에 대 한 후속 호출 HOST_E_CLRNOTAVAILABLE를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e413f-121">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="e413f-122">요구 사항</span><span class="sxs-lookup"><span data-stu-id="e413f-122">Requirements</span></span>  
 <span data-ttu-id="e413f-123">**플랫폼:** 참조 [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="e413f-123">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e413f-124">**헤더:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="e413f-124">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="e413f-125">**라이브러리:** MSCorEE.dll에 리소스로 포함</span><span class="sxs-lookup"><span data-stu-id="e413f-125">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="e413f-126">**.NET framework 버전:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e413f-126">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e413f-127">참고 항목</span><span class="sxs-lookup"><span data-stu-id="e413f-127">See Also</span></span>  
 [<span data-ttu-id="e413f-128">ICLRSyncManager 인터페이스</span><span class="sxs-lookup"><span data-stu-id="e413f-128">ICLRSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrsyncmanager-interface.md)  
 [<span data-ttu-id="e413f-129">IHostAutoEvent 인터페이스</span><span class="sxs-lookup"><span data-stu-id="e413f-129">IHostAutoEvent Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostautoevent-interface.md)  
 [<span data-ttu-id="e413f-130">IHostManualEvent 인터페이스</span><span class="sxs-lookup"><span data-stu-id="e413f-130">IHostManualEvent Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmanualevent-interface.md)  
 [<span data-ttu-id="e413f-131">IHostSyncManager 인터페이스</span><span class="sxs-lookup"><span data-stu-id="e413f-131">IHostSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsyncmanager-interface.md)