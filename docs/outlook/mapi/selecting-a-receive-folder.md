---
title: 受信フォルダーの選択
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 144c7179-b390-479f-a2aa-324974f04eba
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a4245b5dd1b70d4cf695190c65b447cf92566ef7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574483"
---
# <a name="selecting-a-receive-folder"></a><span data-ttu-id="dff9e-103">受信フォルダーの選択</span><span class="sxs-lookup"><span data-stu-id="dff9e-103">Selecting a Receive Folder</span></span>

  
  
<span data-ttu-id="dff9e-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dff9e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dff9e-105">受信フォルダーは、特定クラスの着信メッセージを配置する場所です。</span><span class="sxs-lookup"><span data-stu-id="dff9e-105">A receive folder is where incoming messages of a particular class are placed.</span></span> <span data-ttu-id="dff9e-106">IPM と関連するレポート メッセージは、MAPI では、既定のフォルダーを受信するように、[受信トレイ] が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="dff9e-106">For IPM and related report messages, MAPI assigns the Inbox as the default receive folder.</span></span> <span data-ttu-id="dff9e-107">IPC および関連するレポート メッセージは、MAPI では、既定のフォルダーを受信するようにメッセージ ・ ストアのルート フォルダーが割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="dff9e-107">For IPC and related report messages, MAPI assigns the root folder of the message store as the default receive folder.</span></span> <span data-ttu-id="dff9e-108">これらの割り当てを変更したり、他のメッセージ クラスの追加の割り当てを確認できます。</span><span class="sxs-lookup"><span data-stu-id="dff9e-108">You can change these assignments or make additional assignments for other message classes.</span></span> <span data-ttu-id="dff9e-109">行う明示的な受信フォルダーの割り当て、クライアントでサポートされているクラスは、省略可能なメッセージです。</span><span class="sxs-lookup"><span data-stu-id="dff9e-109">Making explicit receive folder assignments for your client's supported message classes is optional.</span></span>
  
<span data-ttu-id="dff9e-110">受信のメッセージ クラスは、割り当てられている受信フォルダーを持たない場合、メッセージ ストア プロバイダーは自動的に着信クラスの使用可能な最長のプレフィックスと一致するクラスの受信フォルダーを使用します。</span><span class="sxs-lookup"><span data-stu-id="dff9e-110">When an incoming message class does not have an assigned receive folder, the message store provider automatically uses the receive folder for the class that matches the longest possible prefix of the incoming class.</span></span> <span data-ttu-id="dff9e-111">たとえば、次のように、クライアントにはメッセージ クラス IPM の場合です。Note.MyDocument とのみが表示される確立されているフォルダーが IPM メッセージの受信トレイで、このメッセージは、受信トレイにあるため IPM。Note.MyDocument は、IPM の基本クラスから派生します。</span><span class="sxs-lookup"><span data-stu-id="dff9e-111">For example, if your client receives a message of class IPM.Note.MyDocument and the only receive folder that has been established is the Inbox for IPM messages, this message will be placed in the Inbox because IPM.Note.MyDocument derives from the base class IPM.</span></span>
  
<span data-ttu-id="dff9e-112">IPC メッセージの受信フォルダーを割り当てる際は、IPM サブツリーからフォルダーを使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="dff9e-112">When you are assigning a receive folder for IPC messages, never use a folder from the IPM subtree.</span></span> <span data-ttu-id="dff9e-113">IPM メッセージのみ、これらのフォルダーを予約する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dff9e-113">These folders should be reserved for IPM messages only.</span></span> <span data-ttu-id="dff9e-114">メッセージ ストアのルート フォルダー内に含まれているフォルダーを使用します。</span><span class="sxs-lookup"><span data-stu-id="dff9e-114">Use instead a folder that is contained within the message store's root folder.</span></span> 
  
 <span data-ttu-id="dff9e-115">**IPM メッセージ クラスの受信フォルダーを作成するには**</span><span class="sxs-lookup"><span data-stu-id="dff9e-115">**To create a receive folder for an IPM message class**</span></span>
  
1. <span data-ttu-id="dff9e-116">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) のプロパティを取得するために、メッセージ ストアの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="dff9e-116">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property.</span></span> 
    
2. <span data-ttu-id="dff9e-117">開く IPM サブツリーのルート フォルダーにメッセージ ・ ストア内のエントリの識別子としては、 **PR_IPM_SUBTREE_ENTRYID**と[IMsgStore::OpenEntry](imsgstore-openentry.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="dff9e-117">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) with **PR_IPM_SUBTREE_ENTRYID** as the entry identifier to open the root folder of the IPM subtree in the message store.</span></span> 
    
3. <span data-ttu-id="dff9e-118">受信フォルダーを作成するのには[IMAPIFolder::CreateFolder](imapifolder-createfolder.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="dff9e-118">Call [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) to create the receive folder.</span></span> 
    
4. <span data-ttu-id="dff9e-119">IPM メッセージ クラスに新しいフォルダーをマップするのには[IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="dff9e-119">Call [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) to map the new folder to your IPM message class.</span></span> 
    
 <span data-ttu-id="dff9e-120">**IPC メッセージ クラスの受信フォルダーを作成するには**</span><span class="sxs-lookup"><span data-stu-id="dff9e-120">**To create a receive folder for an IPC message class**</span></span>
  
1. <span data-ttu-id="dff9e-121">メッセージ ・ ストアのルート フォルダーを開くに null のエントリの識別子を使用して[IMsgStore::OpenEntry](imsgstore-openentry.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="dff9e-121">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) with a null entry identifier to open the root folder of the message store.</span></span> 
    
2. <span data-ttu-id="dff9e-122">受信フォルダーを作成するのには[IMAPIFolder::CreateFolder](imapifolder-createfolder.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="dff9e-122">Call [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) to create the receive folder.</span></span> 
    
3. <span data-ttu-id="dff9e-123">IPC メッセージ クラスに新しいフォルダーをマップするのには[IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="dff9e-123">Call [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) to map the new folder to your IPC message class.</span></span> 
    
<span data-ttu-id="dff9e-124">関連するレポート メッセージ用のメッセージに使用する受信フォルダーを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="dff9e-124">Assign the receive folder that you use for messages for related report messages.</span></span> <span data-ttu-id="dff9e-125">IPM をクライアントが受信した場合などです。注意のメッセージのいずれかを設定では、将来の IPM のフォルダーが表示されます。注意のメッセージと同じ Report.IPM.Note のメッセージ用のフォルダーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="dff9e-125">For example, if your client receives IPM.Note messages, set up one receive folder for future IPM.Note messages and the same receive folder for future Report.IPM.Note messages.</span></span>
  

