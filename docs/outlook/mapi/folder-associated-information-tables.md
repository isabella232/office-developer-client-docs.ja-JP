---
title: Folder-Associated情報テーブル
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
# <a name="folder-associated-information-tables"></a><span data-ttu-id="4983e-103">Folder-Associated情報テーブル</span><span class="sxs-lookup"><span data-stu-id="4983e-103">Folder-Associated Information Tables</span></span>

  
  
<span data-ttu-id="4983e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4983e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4983e-105">MAPI では、関連する情報MAPI_ASSOCIATED処理するときに使用するさまざまな MAPI コンポーネントのフラグを定義します。</span><span class="sxs-lookup"><span data-stu-id="4983e-105">MAPI defines the MAPI_ASSOCIATED flag for various MAPI components to use when dealing with associated information tables.</span></span> <span data-ttu-id="4983e-106">メッセージ ストア内の各フォルダーには、標準コンテンツ テーブルと共に関連付けられたコンテンツ テーブルが必要です。</span><span class="sxs-lookup"><span data-stu-id="4983e-106">Each folder in a message store should have an associated contents table along with its standard contents table.</span></span> <span data-ttu-id="4983e-107">クライアント アプリケーションは、フォームとビューを保持するために、フォルダーに関連付けられたコンテンツ テーブルに特別なメッセージを格納します。</span><span class="sxs-lookup"><span data-stu-id="4983e-107">Client applications store special messages in a folder's associated contents table to hold forms and views.</span></span> <span data-ttu-id="4983e-108">実際、フォームとビューをサポートするには、メッセージ ストア プロバイダーが関連付けられたコンテンツ テーブルを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4983e-108">In fact, to support forms and views, your message store provider must implement associated contents tables.</span></span>
  
<span data-ttu-id="4983e-109">関連付けられたコンテンツ テーブルを実装するには、ストア プロバイダーが次の操作を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="4983e-109">To implement associated contents tables, your store provider must do the following:</span></span>
  
- <span data-ttu-id="4983e-110">[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)メソッドで MAPI_ASSOCIATED フラグをサポートし、クライアント アプリケーションが標準コンテンツ テーブルの代わりにフォルダーの関連コンテンツ テーブルを取得できます。</span><span class="sxs-lookup"><span data-stu-id="4983e-110">Support the MAPI_ASSOCIATED flag in the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method so client applications can get the folder's associated contents table instead of the standard contents table.</span></span> 
    
- <span data-ttu-id="4983e-111">[IMAPIFolder::CreateMessage](imapifolder-createmessage.md)メソッドで MAPI_ASSOCIATED フラグをサポートし、クライアント アプリケーションがフォルダーの関連付けられたコンテンツ テーブルにメッセージを追加できます。</span><span class="sxs-lookup"><span data-stu-id="4983e-111">Support the MAPI_ASSOCIATED flag in the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method so client applications can add messages to a folder's associated contents table.</span></span> 
    
- <span data-ttu-id="4983e-112">フォルダー オブジェクトの MAPI_ACCESS_CREATE_ASSOCIATED **(** [PidTagAccess](pidtagaccess-canonical-property.md)) プロパティPR_ACCESSビットを設定します。</span><span class="sxs-lookup"><span data-stu-id="4983e-112">Set the MAPI_ACCESS_CREATE_ASSOCIATED bit in the **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) property on folder objects.</span></span>
    
- <span data-ttu-id="4983e-113">[IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md)メソッドでDEL_ASSOCIATEDフラグをサポートします。</span><span class="sxs-lookup"><span data-stu-id="4983e-113">Support the DEL_ASSOCIATED flag in the [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md) method.</span></span> 
    
- <span data-ttu-id="4983e-114">関連付けられたMSGFLAG_ASSOCIATED内のメッセージの PR_MESSAGE_FLAGS **(** [PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティのビットを設定します。</span><span class="sxs-lookup"><span data-stu-id="4983e-114">Set the MSGFLAG_ASSOCIATED bit in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property for messages in the associated contents table.</span></span>
    
- <span data-ttu-id="4983e-115">フォルダーのプロパティ **PR_FOLDER_ASSOCIATED_CONTENTS** [(PidTagFolderAssociatedContents) プロパティ (PidTagFolderAssociatedContents)](pidtagfolderassociatedcontents-canonical-property.md)を公開し、そのプロパティに応答します。</span><span class="sxs-lookup"><span data-stu-id="4983e-115">Expose and respond to the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property on folders.</span></span>
    
- <span data-ttu-id="4983e-116">フォルダーの PR_ASSOC_CONTENT_COUNT ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)) プロパティを維持します。</span><span class="sxs-lookup"><span data-stu-id="4983e-116">Maintain the **PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)) property on folders.</span></span>
    
<span data-ttu-id="4983e-117">メッセージ ストア プロバイダーが関連付けられたコンテンツ **テーブルを** サポートするかどうかをPR_STORE_SUPPORT_MASK ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティにビットはありません。</span><span class="sxs-lookup"><span data-stu-id="4983e-117">There is no bit in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property to indicate whether your message store provider supports associated contents tables.</span></span> <span data-ttu-id="4983e-118">メッセージ ストア プロバイダーがそれらをサポートしていない場合は、クライアント アプリケーションが MAPI_E_NO_SUPPORT フラグを指定して上記のメソッドを呼び出した場合に、MAPI_ASSOCIATED を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="4983e-118">If your message store provider does not support them, it should return MAPI_E_NO_SUPPORT when client applications call any of the above methods with the MAPI_ASSOCIATED flag.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4983e-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="4983e-119">See also</span></span>



<span data-ttu-id="4983e-120">[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)</span><span class="sxs-lookup"><span data-stu-id="4983e-120">[Message Store Features](message-store-features.md)</span></span>

