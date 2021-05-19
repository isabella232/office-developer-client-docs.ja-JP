---
title: 添付がブロックされていることを確認する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 69663470-45f3-86ed-e015-eba32b5a7233
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: c1c6f960f2e24108bebdc8f6cbf08bf1d94d85ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345886"
---
# <a name="verify-an-attachment-is-blocked"></a><span data-ttu-id="5a450-103">添付がブロックされていることを確認する</span><span class="sxs-lookup"><span data-stu-id="5a450-103">Verify an attachment is blocked</span></span>

<span data-ttu-id="5a450-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a450-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a450-105">C++ のこのコード サンプルは[、IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md)インターフェイスを使用して、Microsoft Outlook 2010 または Microsoft Outlook 2013 が表示およびインデックス作成のために添付ファイルをブロックするかどうかを確認する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5a450-105">This code sample in C++ shows how to use the [IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) interface to find out whether an attachment is blocked by Microsoft Outlook 2010 or Microsoft Outlook 2013 for viewing and indexing.</span></span> 
  
<span data-ttu-id="5a450-106">[IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) は [IUnknown インターフェイスから派生](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) します。</span><span class="sxs-lookup"><span data-stu-id="5a450-106">[IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) is derived from the [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) interface.</span></span> <span data-ttu-id="5a450-107">[IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md)インターフェイスを取得するには、MAPI セッション オブジェクトで [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)を呼び出し、そのインターフェイスを要求 **IID_IAttachmentSecurity。**</span><span class="sxs-lookup"><span data-stu-id="5a450-107">You can obtain the [IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) interface by calling [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) on the MAPI session object, requesting **IID_IAttachmentSecurity**.</span></span> <span data-ttu-id="5a450-108">[IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md)は、添付ファイルが Outlook 2010 または Outlook 2013 によって安全でないと見なされ、Outlook 2010 または Outlook 2013 で表示およびインデックス作成がブロックされている場合 _、pfBlocked_ で true を返します。</span><span class="sxs-lookup"><span data-stu-id="5a450-108">[IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) returns **true** in  _pfBlocked_ if the attachment is considered unsafe by Outlook 2010 or Outlook 2013 and is blocked for viewing and indexing in Outlook 2010 or Outlook 2013.</span></span> 
  
```cpp
HRESULT IsAttachmentBlocked(LPMAPISESSION lpMAPISession, LPCWSTR pwszFileName, BOOL* pfBlocked) 
{ 
    if (!lpMAPISession || !pwszFileName || !pfBlocked) return MAPI_E_INVALID_PARAMETER; 
 
    HRESULT hRes = S_OK; 
    IAttachmentSecurity* lpAttachSec = NULL; 
    BOOL bBlocked = false; 
 
    hRes = lpMAPISession-&gt;QueryInterface(IID_IAttachmentSecurity,(void**)&amp;lpAttachSec); 
    if (SUCCEEDED(hRes) &amp;&amp; lpAttachSec) 
    { 
        hRes = lpAttachSec-&gt;IsAttachmentBlocked(pwszFileName,&amp;bBlocked); 
    } 
    if (lpAttachSec) lpAttachSec-&gt;Release(); 
 
    *pfBlocked = bBlocked; 
    return hRes; 
}

```


