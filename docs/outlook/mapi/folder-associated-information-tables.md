---
title: フォルダーに関連付けられた情報テーブル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b72a0d36-c489-41d6-af57-72fbf4b7a3f5
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2332c2a2f7eb46816eab5305b73344e25b2832d7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426416"
---
# <a name="folder-associated-information-tables"></a><span data-ttu-id="a8081-103">フォルダーに関連付けられた情報テーブル</span><span class="sxs-lookup"><span data-stu-id="a8081-103">Folder-Associated Information Tables</span></span>

  
  
<span data-ttu-id="a8081-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8081-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8081-105">mapi は、関連する情報テーブルの処理に使用するさまざまな mapi コンポーネントの MAPI_ASSOCIATED フラグを定義します。</span><span class="sxs-lookup"><span data-stu-id="a8081-105">MAPI defines the MAPI_ASSOCIATED flag for various MAPI components to use when dealing with associated information tables.</span></span> <span data-ttu-id="a8081-106">メッセージストア内の各フォルダーには、その標準コンテンツテーブルと共に、関連付けられた contents テーブルが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="a8081-106">Each folder in a message store should have an associated contents table along with its standard contents table.</span></span> <span data-ttu-id="a8081-107">クライアントアプリケーションは、フォームとビューを保持するために、フォルダーに関連付けられた contents テーブルに特別なメッセージを格納します。</span><span class="sxs-lookup"><span data-stu-id="a8081-107">Client applications store special messages in a folder's associated contents table to hold forms and views.</span></span> <span data-ttu-id="a8081-108">実際に、フォームとビューをサポートするには、メッセージストアプロバイダーが関連するコンテンツテーブルを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a8081-108">In fact, to support forms and views, your message store provider must implement associated contents tables.</span></span>
  
<span data-ttu-id="a8081-109">関連するコンテンツテーブルを実装するには、ストアプロバイダーが次のことを行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="a8081-109">To implement associated contents tables, your store provider must do the following:</span></span>
  
- <span data-ttu-id="a8081-110">[IMAPIContainer:: getcontentstable](imapicontainer-getcontentstable.md)メソッドの MAPI_ASSOCIATED フラグをサポートすることにより、クライアントアプリケーションが、標準の contents テーブルではなく、フォルダーに関連付けられたコンテンツテーブルを取得できるようにします。</span><span class="sxs-lookup"><span data-stu-id="a8081-110">Support the MAPI_ASSOCIATED flag in the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method so client applications can get the folder's associated contents table instead of the standard contents table.</span></span> 
    
- <span data-ttu-id="a8081-111">[imapifolder:: CreateMessage](imapifolder-createmessage.md)メソッドの MAPI_ASSOCIATED フラグをサポートすることにより、クライアントアプリケーションがフォルダーに関連付けられたコンテンツテーブルにメッセージを追加できるようにします。</span><span class="sxs-lookup"><span data-stu-id="a8081-111">Support the MAPI_ASSOCIATED flag in the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method so client applications can add messages to a folder's associated contents table.</span></span> 
    
- <span data-ttu-id="a8081-112">folder オブジェクトの**PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) プロパティで MAPI_ACCESS_CREATE_ASSOCIATED ビットを設定します。</span><span class="sxs-lookup"><span data-stu-id="a8081-112">Set the MAPI_ACCESS_CREATE_ASSOCIATED bit in the **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) property on folder objects.</span></span>
    
- <span data-ttu-id="a8081-113">[imapifolder:: emptyfolder](imapifolder-emptyfolder.md)メソッドで DEL_ASSOCIATED フラグをサポートします。</span><span class="sxs-lookup"><span data-stu-id="a8081-113">Support the DEL_ASSOCIATED flag in the [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md) method.</span></span> 
    
- <span data-ttu-id="a8081-114">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティの MSGFLAG_ASSOCIATED ビットを、関連付けられている contents テーブル内のメッセージに設定します。</span><span class="sxs-lookup"><span data-stu-id="a8081-114">Set the MSGFLAG_ASSOCIATED bit in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property for messages in the associated contents table.</span></span>
    
- <span data-ttu-id="a8081-115">フォルダーの**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) プロパティを公開して応答します。</span><span class="sxs-lookup"><span data-stu-id="a8081-115">Expose and respond to the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property on folders.</span></span>
    
- <span data-ttu-id="a8081-116">フォルダーの**PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)) プロパティを維持します。</span><span class="sxs-lookup"><span data-stu-id="a8081-116">Maintain the **PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)) property on folders.</span></span>
    
<span data-ttu-id="a8081-117">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティには、メッセージストアプロバイダーが関連付けられたコンテンツテーブルをサポートしているかどうかを示すビットはありません。</span><span class="sxs-lookup"><span data-stu-id="a8081-117">There is no bit in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property to indicate whether your message store provider supports associated contents tables.</span></span> <span data-ttu-id="a8081-118">メッセージストアプロバイダーがサポートしていない場合は、クライアントアプリケーションが MAPI_ASSOCIATED フラグを使用して上記のいずれかのメソッドを呼び出すと、MAPI_E_NO_SUPPORT が返されます。</span><span class="sxs-lookup"><span data-stu-id="a8081-118">If your message store provider does not support them, it should return MAPI_E_NO_SUPPORT when client applications call any of the above methods with the MAPI_ASSOCIATED flag.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a8081-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="a8081-119">See also</span></span>



<span data-ttu-id="a8081-120">[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)</span><span class="sxs-lookup"><span data-stu-id="a8081-120">[Message Store Features](message-store-features.md)</span></span>

