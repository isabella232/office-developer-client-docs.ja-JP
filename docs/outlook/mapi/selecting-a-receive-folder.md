---
title: 受信フォルダーの選択
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 144c7179-b390-479f-a2aa-324974f04eba
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9151b76f74dead5cac771dbdc091bbee03359aec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428418"
---
# <a name="selecting-a-receive-folder"></a><span data-ttu-id="209f4-103">受信フォルダーの選択</span><span class="sxs-lookup"><span data-stu-id="209f4-103">Selecting a Receive Folder</span></span>

  
  
<span data-ttu-id="209f4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="209f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="209f4-105">受信フォルダーには、特定のクラスの受信メッセージが配置されます。</span><span class="sxs-lookup"><span data-stu-id="209f4-105">A receive folder is where incoming messages of a particular class are placed.</span></span> <span data-ttu-id="209f4-106">IPM および関連するレポートメッセージの場合、MAPI は既定の受信フォルダーとして受信トレイを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="209f4-106">For IPM and related report messages, MAPI assigns the Inbox as the default receive folder.</span></span> <span data-ttu-id="209f4-107">IPC および関連するレポートメッセージの場合、MAPI はメッセージストアのルートフォルダーを既定の受信フォルダーとして割り当てます。</span><span class="sxs-lookup"><span data-stu-id="209f4-107">For IPC and related report messages, MAPI assigns the root folder of the message store as the default receive folder.</span></span> <span data-ttu-id="209f4-108">その他のメッセージクラスについては、これらの割り当てを変更したり、追加の割り当てを行ったりすることができます。</span><span class="sxs-lookup"><span data-stu-id="209f4-108">You can change these assignments or make additional assignments for other message classes.</span></span> <span data-ttu-id="209f4-109">クライアントでサポートされているメッセージクラスに対して明示的な受信フォルダーの割り当てを行うことはオプションです。</span><span class="sxs-lookup"><span data-stu-id="209f4-109">Making explicit receive folder assignments for your client's supported message classes is optional.</span></span>
  
<span data-ttu-id="209f4-110">受信メッセージクラスに、受信フォルダーが割り当てられていない場合、メッセージストアプロバイダーは、受信クラスの可能な最大プレフィックスに一致するクラスの受信フォルダーを自動的に使用します。</span><span class="sxs-lookup"><span data-stu-id="209f4-110">When an incoming message class does not have an assigned receive folder, the message store provider automatically uses the receive folder for the class that matches the longest possible prefix of the incoming class.</span></span> <span data-ttu-id="209f4-111">たとえば、クライアントがクラス IPM というメッセージを受信するとします。メモ: 設定済みの受信フォルダーのみが、ipm メッセージの受信トレイに配置されます。このメッセージは、ipm.注: MyDocument は基本クラス IPM から派生します。</span><span class="sxs-lookup"><span data-stu-id="209f4-111">For example, if your client receives a message of class IPM.Note.MyDocument and the only receive folder that has been established is the Inbox for IPM messages, this message will be placed in the Inbox because IPM.Note.MyDocument derives from the base class IPM.</span></span>
  
<span data-ttu-id="209f4-112">IPC メッセージの受信フォルダーを割り当てる場合は、IPM サブツリーのフォルダーは使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="209f4-112">When you are assigning a receive folder for IPC messages, never use a folder from the IPM subtree.</span></span> <span data-ttu-id="209f4-113">これらのフォルダーは、IPM メッセージ専用に予約されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="209f4-113">These folders should be reserved for IPM messages only.</span></span> <span data-ttu-id="209f4-114">代わりに、メッセージストアのルートフォルダー内に格納されているフォルダーを使用します。</span><span class="sxs-lookup"><span data-stu-id="209f4-114">Use instead a folder that is contained within the message store's root folder.</span></span> 
  
 <span data-ttu-id="209f4-115">**IPM メッセージクラスの受信フォルダーを作成するには**</span><span class="sxs-lookup"><span data-stu-id="209f4-115">**To create a receive folder for an IPM message class**</span></span>
  
1. <span data-ttu-id="209f4-116">メッセージストアの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出して、 **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="209f4-116">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property.</span></span> 
    
2. <span data-ttu-id="209f4-117">[IMsgStore:: openentry](imsgstore-openentry.md)を entry 識別子として**PR_IPM_SUBTREE_ENTRYID**で呼び出し、メッセージストア内の IPM サブツリーのルートフォルダーを開きます。</span><span class="sxs-lookup"><span data-stu-id="209f4-117">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) with **PR_IPM_SUBTREE_ENTRYID** as the entry identifier to open the root folder of the IPM subtree in the message store.</span></span> 
    
3. <span data-ttu-id="209f4-118">[imapifolder:: CreateFolder](imapifolder-createfolder.md)を呼び出して、受信フォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="209f4-118">Call [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) to create the receive folder.</span></span> 
    
4. <span data-ttu-id="209f4-119">[IMsgStore:: setreceivefolder](imsgstore-setreceivefolder.md)を呼び出して、新しいフォルダーを IPM メッセージクラスにマップします。</span><span class="sxs-lookup"><span data-stu-id="209f4-119">Call [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) to map the new folder to your IPM message class.</span></span> 
    
 <span data-ttu-id="209f4-120">**IPC メッセージクラスの受信フォルダーを作成するには**</span><span class="sxs-lookup"><span data-stu-id="209f4-120">**To create a receive folder for an IPC message class**</span></span>
  
1. <span data-ttu-id="209f4-121">[IMsgStore::](imsgstore-openentry.md) null エントリ識別子を持つ openentry を呼び出して、メッセージストアのルートフォルダーを開きます。</span><span class="sxs-lookup"><span data-stu-id="209f4-121">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) with a null entry identifier to open the root folder of the message store.</span></span> 
    
2. <span data-ttu-id="209f4-122">[imapifolder:: CreateFolder](imapifolder-createfolder.md)を呼び出して、受信フォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="209f4-122">Call [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) to create the receive folder.</span></span> 
    
3. <span data-ttu-id="209f4-123">[IMsgStore:: setreceivefolder](imsgstore-setreceivefolder.md)を呼び出して、新しいフォルダーを IPC メッセージクラスにマップします。</span><span class="sxs-lookup"><span data-stu-id="209f4-123">Call [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) to map the new folder to your IPC message class.</span></span> 
    
<span data-ttu-id="209f4-124">関連するレポートメッセージのメッセージに使用する受信フォルダーを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="209f4-124">Assign the receive folder that you use for messages for related report messages.</span></span> <span data-ttu-id="209f4-125">たとえば、クライアントが IPM を受信したとします。メッセージを確認し、今後の IPM 用に1つの受信フォルダーをセットアップします。メモメッセージと、今後の報告メッセージの同じ受信フォルダー。</span><span class="sxs-lookup"><span data-stu-id="209f4-125">For example, if your client receives IPM.Note messages, set up one receive folder for future IPM.Note messages and the same receive folder for future Report.IPM.Note messages.</span></span>
  

