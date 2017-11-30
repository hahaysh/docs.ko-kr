---
title: "ISymUnmanagedSourceServerModule 인터페이스"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ISymUnmanagedSourceServerModule
api_location: diasymreader.dll
api_type: COM
f1_keywords: ISymUnmanagedSourceServerModule
helpviewer_keywords: ISymUnmanagedSourceServerModule interface [.NET Framework debugging]
ms.assetid: a19b23bd-2061-476e-b67d-252f57404f8b
topic_type: apiref
caps.latest.revision: "6"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 3110be6a42ce68a6a8b3571206244a7fd1d38b8a
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/18/2017
---
# <a name="isymunmanagedsourceservermodule-interface"></a><span data-ttu-id="f46d1-102">ISymUnmanagedSourceServerModule 인터페이스</span><span class="sxs-lookup"><span data-stu-id="f46d1-102">ISymUnmanagedSourceServerModule Interface</span></span>
<span data-ttu-id="f46d1-103">모듈에 대 한 원본 서버 데이터를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="f46d1-103">Provides source server data for a module.</span></span> <span data-ttu-id="f46d1-104">이 인터페이스를 호출 하 여 가져올 `QueryInterface` 구현 하는 개체에는 [ISymUnmanagedReader](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md) 인터페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="f46d1-104">Obtain this interface by calling `QueryInterface` on an object that implements the [ISymUnmanagedReader](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md) interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="f46d1-105">메서드</span><span class="sxs-lookup"><span data-stu-id="f46d1-105">Methods</span></span>  
  
|<span data-ttu-id="f46d1-106">메서드</span><span class="sxs-lookup"><span data-stu-id="f46d1-106">Method</span></span>|<span data-ttu-id="f46d1-107">설명</span><span class="sxs-lookup"><span data-stu-id="f46d1-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="f46d1-108">GetSourceServerData 메서드</span><span class="sxs-lookup"><span data-stu-id="f46d1-108">GetSourceServerData Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedsourceservermodule-getsourceserverdata-method.md)|<span data-ttu-id="f46d1-109">모듈에 대 한 원본 서버 데이터를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f46d1-109">Returns the source server data for the module.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="f46d1-110">요구 사항</span><span class="sxs-lookup"><span data-stu-id="f46d1-110">Requirements</span></span>  
 <span data-ttu-id="f46d1-111">**헤더:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="f46d1-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f46d1-112">참고 항목</span><span class="sxs-lookup"><span data-stu-id="f46d1-112">See Also</span></span>  
 [<span data-ttu-id="f46d1-113">진단 기호 저장소 인터페이스</span><span class="sxs-lookup"><span data-stu-id="f46d1-113">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)