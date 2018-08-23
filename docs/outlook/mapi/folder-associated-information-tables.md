---
title: フォルダー関連情報テーブル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b72a0d36-c489-41d6-af57-72fbf4b7a3f5
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 09cac591aac9d266571348531e378974b86a3a9d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800088"
---
# <a name="folder-associated-information-tables"></a><span data-ttu-id="36d8f-103">フォルダー関連情報テーブル</span><span class="sxs-lookup"><span data-stu-id="36d8f-103">Folder-Associated Information Tables</span></span>

  
  
<span data-ttu-id="36d8f-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="36d8f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="36d8f-105">MAPI では、関連する情報のテーブルを処理するときに使用する各種の MAPI コンポーネントの MAPI_ASSOCIATED フラグを定義します。</span><span class="sxs-lookup"><span data-stu-id="36d8f-105">MAPI defines the MAPI_ASSOCIATED flag for various MAPI components to use when dealing with associated information tables.</span></span> <span data-ttu-id="36d8f-106">メッセージ ・ ストア内の各フォルダーには、標準的な内容のテーブルと、関連する内容のテーブルが必要です。</span><span class="sxs-lookup"><span data-stu-id="36d8f-106">Each folder in a message store should have an associated contents table along with its standard contents table.</span></span> <span data-ttu-id="36d8f-107">クライアント アプリケーションでは、フォームとビューを保持するためにフォルダーの内容が関連付けられているテーブルに特別なメッセージを保存します。</span><span class="sxs-lookup"><span data-stu-id="36d8f-107">Client applications store special messages in a folder's associated contents table to hold forms and views.</span></span> <span data-ttu-id="36d8f-108">実際には、フォームとビューをサポートするため、メッセージ ストア プロバイダーは、関連付けられている内容のテーブルを実装しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="36d8f-108">In fact, to support forms and views, your message store provider must implement associated contents tables.</span></span>
  
<span data-ttu-id="36d8f-109">コンテンツが関連付けられているテーブルを実装するには、ストア プロバイダーは、次の。</span><span class="sxs-lookup"><span data-stu-id="36d8f-109">To implement associated contents tables, your store provider must do the following:</span></span>
  
- <span data-ttu-id="36d8f-110">[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)メソッドで MAPI_ASSOCIATED フラグをサポートし、ため、クライアント アプリケーションは、標準的な内容のテーブルではなく、フォルダーの内容が関連付けられているテーブルを取得できます。</span><span class="sxs-lookup"><span data-stu-id="36d8f-110">Support the MAPI_ASSOCIATED flag in the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method so client applications can get the folder's associated contents table instead of the standard contents table.</span></span> 
    
- <span data-ttu-id="36d8f-111">クライアント アプリケーションは、フォルダーの内容が関連付けられているテーブルにメッセージを追加できるように、 [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)メソッドで MAPI_ASSOCIATED フラグをサポートします。</span><span class="sxs-lookup"><span data-stu-id="36d8f-111">Support the MAPI_ASSOCIATED flag in the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method so client applications can add messages to a folder's associated contents table.</span></span> 
    
- <span data-ttu-id="36d8f-112">**PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) のプロパティのフォルダー オブジェクトに MAPI_ACCESS_CREATE_ASSOCIATED ビットを設定します。</span><span class="sxs-lookup"><span data-stu-id="36d8f-112">Set the MAPI_ACCESS_CREATE_ASSOCIATED bit in the **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) property on folder objects.</span></span>
    
- <span data-ttu-id="36d8f-113">[IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md)メソッドで、DEL_ASSOCIATED フラグをサポートします。</span><span class="sxs-lookup"><span data-stu-id="36d8f-113">Support the DEL_ASSOCIATED flag in the [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md) method.</span></span> 
    
- <span data-ttu-id="36d8f-114">MSGFLAG_ASSOCIATED の**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) は、関連付けられているコンテンツ」テーブル内のメッセージのビットを設定します。</span><span class="sxs-lookup"><span data-stu-id="36d8f-114">Set the MSGFLAG_ASSOCIATED bit in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property for messages in the associated contents table.</span></span>
    
- <span data-ttu-id="36d8f-115">公開し、フォルダーの**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) のプロパティに対応します。</span><span class="sxs-lookup"><span data-stu-id="36d8f-115">Expose and respond to the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property on folders.</span></span>
    
- <span data-ttu-id="36d8f-116">フォルダーの**PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)) のプロパティを保持します。</span><span class="sxs-lookup"><span data-stu-id="36d8f-116">Maintain the **PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)) property on folders.</span></span>
    
<span data-ttu-id="36d8f-117">メッセージ ストア プロバイダーが関連付けられている内容のテーブルをサポートしているかどうかを示すために**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティでは、ビットはありません。</span><span class="sxs-lookup"><span data-stu-id="36d8f-117">There is no bit in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property to indicate whether your message store provider supports associated contents tables.</span></span> <span data-ttu-id="36d8f-118">メッセージ ストア プロバイダーではサポートしていない場合、クライアント アプリケーションでは、MAPI_ASSOCIATED フラグを使用して上記の方法のいずれかを呼び出すと、MAPI_E_NO_SUPPORT を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="36d8f-118">If your message store provider does not support them, it should return MAPI_E_NO_SUPPORT when client applications call any of the above methods with the MAPI_ASSOCIATED flag.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="36d8f-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="36d8f-119">See also</span></span>



<span data-ttu-id="36d8f-120">[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)</span><span class="sxs-lookup"><span data-stu-id="36d8f-120">[Message Store Features](message-store-features.md)</span></span>

