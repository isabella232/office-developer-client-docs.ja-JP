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
# <a name="selecting-a-receive-folder"></a><span data-ttu-id="1690c-103">受信フォルダーの選択</span><span class="sxs-lookup"><span data-stu-id="1690c-103">Selecting a Receive Folder</span></span>

  
  
<span data-ttu-id="1690c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1690c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1690c-105">受信フォルダーは、特定のクラスの受信メッセージが配置される場所です。</span><span class="sxs-lookup"><span data-stu-id="1690c-105">A receive folder is where incoming messages of a particular class are placed.</span></span> <span data-ttu-id="1690c-106">IPM および関連するレポート メッセージの場合、MAPI は受信トレイを既定の受信フォルダーとして割り当てる。</span><span class="sxs-lookup"><span data-stu-id="1690c-106">For IPM and related report messages, MAPI assigns the Inbox as the default receive folder.</span></span> <span data-ttu-id="1690c-107">IPC および関連するレポート メッセージの場合、MAPI はメッセージ ストアのルート フォルダーを既定の受信フォルダーとして割り当てる。</span><span class="sxs-lookup"><span data-stu-id="1690c-107">For IPC and related report messages, MAPI assigns the root folder of the message store as the default receive folder.</span></span> <span data-ttu-id="1690c-108">これらの割り当てを変更するか、他のメッセージ クラスに追加の割り当てを行います。</span><span class="sxs-lookup"><span data-stu-id="1690c-108">You can change these assignments or make additional assignments for other message classes.</span></span> <span data-ttu-id="1690c-109">クライアントでサポートされているメッセージ クラスに対して明示的な受信フォルダーの割り当てを行う方法はオプションです。</span><span class="sxs-lookup"><span data-stu-id="1690c-109">Making explicit receive folder assignments for your client's supported message classes is optional.</span></span>
  
<span data-ttu-id="1690c-110">受信メッセージ クラスに受信フォルダーが割り当てられていない場合、メッセージ ストア プロバイダーは、受信クラスの可能な限り長いプレフィックスに一致するクラスの受信フォルダーを自動的に使用します。</span><span class="sxs-lookup"><span data-stu-id="1690c-110">When an incoming message class does not have an assigned receive folder, the message store provider automatically uses the receive folder for the class that matches the longest possible prefix of the incoming class.</span></span> <span data-ttu-id="1690c-111">たとえば、クライアントがクラス IPM のメッセージを受信した場合です。Note.MyDocument と確立された受信フォルダーは IPM メッセージの受信トレイのみです。このメッセージは IPM のため受信トレイに配置されます。Note.MyDocument は、基本クラス IPM から派生します。</span><span class="sxs-lookup"><span data-stu-id="1690c-111">For example, if your client receives a message of class IPM.Note.MyDocument and the only receive folder that has been established is the Inbox for IPM messages, this message will be placed in the Inbox because IPM.Note.MyDocument derives from the base class IPM.</span></span>
  
<span data-ttu-id="1690c-112">IPC メッセージの受信フォルダーを割り当てる場合は、IPM サブツリーのフォルダーを使用しません。</span><span class="sxs-lookup"><span data-stu-id="1690c-112">When you are assigning a receive folder for IPC messages, never use a folder from the IPM subtree.</span></span> <span data-ttu-id="1690c-113">これらのフォルダーは、IPM メッセージ専用に予約する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1690c-113">These folders should be reserved for IPM messages only.</span></span> <span data-ttu-id="1690c-114">代わりに、メッセージ ストアのルート フォルダー内に含まれるフォルダーを使用します。</span><span class="sxs-lookup"><span data-stu-id="1690c-114">Use instead a folder that is contained within the message store's root folder.</span></span> 
  
 <span data-ttu-id="1690c-115">**IPM メッセージ クラスの受信フォルダーを作成するには**</span><span class="sxs-lookup"><span data-stu-id="1690c-115">**To create a receive folder for an IPM message class**</span></span>
  
1. <span data-ttu-id="1690c-116">メッセージ ストアの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出して、PR_IPM_SUBTREE_ENTRYID **(** [PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="1690c-116">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property.</span></span> 
    
2. <span data-ttu-id="1690c-117">メッセージ ストアで IPM サブ **ツリー** のルート フォルダーを開PR_IPM_SUBTREE_ENTRYID ID として [IMsgStore::OpenEntry](imsgstore-openentry.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1690c-117">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) with **PR_IPM_SUBTREE_ENTRYID** as the entry identifier to open the root folder of the IPM subtree in the message store.</span></span> 
    
3. <span data-ttu-id="1690c-118">[IMAPIFolder::CreateFolder を呼び出して](imapifolder-createfolder.md)受信フォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="1690c-118">Call [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) to create the receive folder.</span></span> 
    
4. <span data-ttu-id="1690c-119">[IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md)を呼び出して、新しいフォルダーを IPM メッセージ クラスにマップします。</span><span class="sxs-lookup"><span data-stu-id="1690c-119">Call [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) to map the new folder to your IPM message class.</span></span> 
    
 <span data-ttu-id="1690c-120">**IPC メッセージ クラスの受信フォルダーを作成するには**</span><span class="sxs-lookup"><span data-stu-id="1690c-120">**To create a receive folder for an IPC message class**</span></span>
  
1. <span data-ttu-id="1690c-121">メッセージ ストアのルート フォルダーを開く場合は、NULL エントリ識別子を使用して [IMsgStore::OpenEntry](imsgstore-openentry.md) を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1690c-121">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) with a null entry identifier to open the root folder of the message store.</span></span> 
    
2. <span data-ttu-id="1690c-122">[IMAPIFolder::CreateFolder を呼び出して](imapifolder-createfolder.md)受信フォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="1690c-122">Call [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) to create the receive folder.</span></span> 
    
3. <span data-ttu-id="1690c-123">[IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md)を呼び出して、新しいフォルダーを IPC メッセージ クラスにマップします。</span><span class="sxs-lookup"><span data-stu-id="1690c-123">Call [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) to map the new folder to your IPC message class.</span></span> 
    
<span data-ttu-id="1690c-124">関連するレポート メッセージのメッセージに使用する受信フォルダーを割り当てる。</span><span class="sxs-lookup"><span data-stu-id="1690c-124">Assign the receive folder that you use for messages for related report messages.</span></span> <span data-ttu-id="1690c-125">たとえば、クライアントが IPM を受信した場合です。メモ メッセージは、将来の IPM 用に 1 つの受信フォルダーを設定します。メッセージと、将来の Report.IPM.Note メッセージ用の同じ受信フォルダーをメモします。</span><span class="sxs-lookup"><span data-stu-id="1690c-125">For example, if your client receives IPM.Note messages, set up one receive folder for future IPM.Note messages and the same receive folder for future Report.IPM.Note messages.</span></span>
  

