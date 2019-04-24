---
title: POP3 アカウントのメッセージ ダウンロード履歴の検索
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 90a51150-5c2c-4d5b-8717-5dacc8532744
description: このトピックでは、メールクライアントが PidTagAttachDataBinary プロパティにアクセスして、POP3 アカウントのメッセージのダウンロード履歴を取得する方法について説明します。
ms.openlocfilehash: ae12a044098aa4f42e1c2e5936e82da3d7a128dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321876"
---
# <a name="locating-the-message-download-history-for-a-pop3-account"></a><span data-ttu-id="5f5fe-103">POP3 アカウントのメッセージ ダウンロード履歴の検索</span><span class="sxs-lookup"><span data-stu-id="5f5fe-103">Locating the message download history for a POP3 account</span></span>

<span data-ttu-id="5f5fe-104">このトピックでは、メールクライアントが[PidTagAttachDataBinary](https://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx)プロパティにアクセスして、POP3 アカウントのメッセージのダウンロード履歴を取得する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-104">This topic describes how a mail client can access the [PidTagAttachDataBinary](https://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx) property to get the message download history for a POP3 account.</span></span> 

<span data-ttu-id="5f5fe-105"><a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_WhyGetUIDLHistory"> </a></span><span class="sxs-lookup"><span data-stu-id="5f5fe-105"></span></span>

## <a name="why-get-the-message-download-history"></a><span data-ttu-id="5f5fe-106">メッセージのダウンロード履歴を取得する理由</span><span class="sxs-lookup"><span data-stu-id="5f5fe-106">Why get the message download history?</span></span>

<span data-ttu-id="5f5fe-107">Outlook の Post Office Protocol (POP) プロバイダーを使用すると、ユーザーは新しい電子メールメッセージをローカルデバイスで取得してダウンロードし、メールサーバー上でこれらの電子メールメッセージを残すか削除することができます。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-107">The Post Office Protocol (POP) provider for Outlook allows users to retrieve and download new email messages on their local device, and subsequently to leave or delete these email messages on the mail server.</span></span> <span data-ttu-id="5f5fe-108">メールクライアントは、新しいメッセージのダウンロードを確認するときに、その受信トレイの新しいメッセージのみを識別してダウンロードできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-108">When the mail client checks for new messages to download, it has to be able to identify and download only the new messages for that Inbox.</span></span> <span data-ttu-id="5f5fe-109">メールクライアントはまず、UIDL (一意の ID リスト) コマンドを使用して、その受信トレイに配信された各メッセージのマップを一意の識別子 (UID) に取得します。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-109">The mail client does this by first using the UIDL (Unique ID Listing) command, which obtains a map of each message that has ever been delivered to that Inbox to a unique identifier (UID).</span></span> <span data-ttu-id="5f5fe-110">クライアントは、そのクライアント上で受信トレイに対してダウンロードまたは削除されたメッセージのメッセージダウンロード履歴も取得します。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-110">The client also gets the message download history for messages that have been downloaded or deleted for the Inbox on that client.</span></span> <span data-ttu-id="5f5fe-111">メッセージ UID マップとダウンロード履歴を使用して、クライアントは履歴内に存在しないメッセージを新規として識別できるため、ダウンロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-111">Using the message UID map and download history, the client can then identify those messages that are absent in the history as new and, hence, should be downloaded.</span></span>
  
<span data-ttu-id="5f5fe-112">受信トレイのメッセージダウンロード履歴を取得するには、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-112">To get the message download history for an Inbox:</span></span>
  
- <span data-ttu-id="5f5fe-113">このトピックの手順に従って**PidTagAttachDataBinary**プロパティを検索します。これには、特定の形式に従ったバイナリラージオブジェクト (BLOB) 内の履歴が含まれます。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-113">Follow the steps in this topic to find the **PidTagAttachDataBinary** property, which contains the history in a binary large object (BLOB) that follows a specific format.</span></span> 
    
- <span data-ttu-id="5f5fe-114">次に、 [POP3 アカウントのメッセージダウンロード履歴の解析](parsing-the-message-download-history-for-a-pop3-account.md)を続けます。この BLOB を解析して、その受信トレイでダウンロードまたは削除されたメッセージを識別する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-114">Continue with [Parsing the message download history for a POP3 account](parsing-the-message-download-history-for-a-pop3-account.md), which describes how to parse this BLOB to identify messages that have been downloaded or deleted for that Inbox.</span></span>
    
## <a name="core-concepts-to-know-for-locating-the-message-download-history"></a><span data-ttu-id="5f5fe-115">メッセージのダウンロード履歴を検索する際に知っておく必要がある中心概念</span><span class="sxs-lookup"><span data-stu-id="5f5fe-115">Core concepts to know for locating the message download history</span></span>

<span data-ttu-id="5f5fe-116">受信トレイのメッセージのダウンロード履歴は、受信トレイ内の非表示のメッセージの添付ファイルにある**PidTagAttachDataBinary**というバイナリ MAPI プロパティに格納されます。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-116">The message download history for an Inbox is stored in a binary MAPI property, **PidTagAttachDataBinary**, on an attachment of a hidden message in the Inbox.</span></span> <span data-ttu-id="5f5fe-117">表1は、メッセージのダウンロード履歴を見つける方法を理解するのに役立つ概念のリソースを示しています。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-117">Table 1 shows resources for concepts that help you understand how to locate the message download history.</span></span>
  
<span data-ttu-id="5f5fe-118">**表 1. 中心概念**</span><span class="sxs-lookup"><span data-stu-id="5f5fe-118">**Table 1. Core concepts**</span></span>

|<span data-ttu-id="5f5fe-119">**記事のタイトル**</span><span class="sxs-lookup"><span data-stu-id="5f5fe-119">**Article title**</span></span>|<span data-ttu-id="5f5fe-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="5f5fe-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5f5fe-121">MAPI の隠しフォルダー</span><span class="sxs-lookup"><span data-stu-id="5f5fe-121">MAPI Hidden Folders</span></span>](https://msdn.microsoft.com/library/8b3b9c80-f7f4-4f37-bd6b-323469d020f1%28Office.15%29.aspx) <br/> |<span data-ttu-id="5f5fe-122">MAPI では、メールクライアントが非表示のフォルダーおよび非表示のメッセージに情報を格納することができます。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-122">MAPI allows mail clients to store information in hidden folders and hidden messages.</span></span> <span data-ttu-id="5f5fe-123">隠しフォルダーは MAPI フォルダーの関連部分にあり、通常、ユーザーが操作することはできず、表示されない情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-123">Hidden folders are in the associated part of MAPI folders and typically contain information that is not visible to and not to be manipulated by users.</span></span> <span data-ttu-id="5f5fe-124">クライアントは、隠しメッセージに隠しフォルダーに格納するための形式と内容を決定します。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-124">Clients decide the format and contents to store in hidden messages in hidden folders.</span></span>  <br/> |
|[<span data-ttu-id="5f5fe-125">MAPI メッセージ</span><span class="sxs-lookup"><span data-stu-id="5f5fe-125">MAPI Messages</span></span>](https://msdn.microsoft.com/library/417c113f-bd98-4515-85d1-09db7fc3a227%28Office.15%29.aspx) <br/> |<span data-ttu-id="5f5fe-126">MAPI は、クライアントのユーザーに対して表示される標準の IPM サブツリー、またはサブツリーの外部にあるフォルダーにメッセージを格納し、ユーザーには見えません。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-126">MAPI stores messages in folders, either in the standard IPM subtree that is visible to users of a client, or outside of the subtree and invisible to users.</span></span> <span data-ttu-id="5f5fe-127">メッセージには添付ファイルに格納される追加のデータを含めることができます。これは、ファイル、別のメッセージ、または OLE オブジェクトの形式にすることができます。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-127">Messages can have additional data stored in an attachment, which can be in the form of a file, another message, or an OLE object.</span></span> <span data-ttu-id="5f5fe-128">メッセージのダウンロード履歴の場合、履歴は別の非表示メッセージに添付されたメッセージのプロパティに格納されます。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-128">In the case of the message download history, the history is stored in a property of a message that is attached to another hidden message.</span></span>  <br/> |
|[<span data-ttu-id="5f5fe-129">メッセージプロパティの概要</span><span class="sxs-lookup"><span data-stu-id="5f5fe-129">Message Properties Overview</span></span>](https://msdn.microsoft.com/library/447f54de-9f0d-4f73-89b6-bed9cfea9c15%28Office.15%29.aspx) <br/> |<span data-ttu-id="5f5fe-130">クライアントは、メッセージに情報を格納するときに、実際にはメッセージのプロパティに情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-130">When a client stores information in a message, it actually stores the information in a property of the message.</span></span> <span data-ttu-id="5f5fe-131">MAPI は多くのプロパティをサポートしています。一部は常に存在し、クライアントによって設定できます。その他はオプションであり、クライアントはそれらを利用できない、または有効な値に設定することを想定できません。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-131">MAPI supports many properties—some always exist and can be set by clients, others are optional—and clients cannot expect them to be available or set to valid values.</span></span> <span data-ttu-id="5f5fe-132">メッセージのダウンロード履歴は、非表示のメッセージの添付ファイルの**PidTagAttachDataBinary**プロパティに格納されます。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-132">The message download history is stored in the **PidTagAttachDataBinary** property of an attachment to a hidden message.</span></span>  <br/> |
|[<span data-ttu-id="5f5fe-133">MAPI プロファイル</span><span class="sxs-lookup"><span data-stu-id="5f5fe-133">MAPI Profiles</span></span>](https://msdn.microsoft.com/library/493c87a4-317d-47ec-850b-342cac59594b%28Office.15%29.aspx) <br/> |<span data-ttu-id="5f5fe-134">セッションのログオン時に、メールクライアントは、使用するプロバイダーとサービスを記述するプロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-134">At logon time in a session, the mail client selects a profile that describes the providers and services to be used.</span></span> <span data-ttu-id="5f5fe-135">プロファイルは、プロパティを含むセクションに分かれています。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-135">A profile is divided into sections that contain properties.</span></span> <span data-ttu-id="5f5fe-136">特に、 [PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) (**PR_SEARCH_KEY**) および[PidTagProfileName](https://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx) (**PR_PROFILE_NAME**) プロパティは常に存在します。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-136">In particular, the [PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) (**PR_SEARCH_KEY**) and [PidTagProfileName](https://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx) (**PR_PROFILE_NAME**) properties always exist.</span></span> <span data-ttu-id="5f5fe-137">プロファイルの検索キーは、すべてのプロファイルで一意であり、 **MUID_PROFILE_INSTANCE**によって識別されるプロファイルセクションに格納されます (mapiguid で定義されています)。H)。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-137">A profile's search key is unique among all profiles, and is stored in the profile section that is identified by **MUID_PROFILE_INSTANCE** (which is defined in MAPIGUID.H).</span></span> <span data-ttu-id="5f5fe-138">[imapisession:: openプロファイル](https://msdn.microsoft.com/library/e2757028-27e7-4fc0-9674-e8e30737ef1d%28Office.15%29.aspx)を使用してセクションを開き、 [imapisession:: GetProps](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx)を使用してプロパティ値を取得します。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-138">Use [IMAPISession::OpenProfileSection](https://msdn.microsoft.com/library/e2757028-27e7-4fc0-9674-e8e30737ef1d%28Office.15%29.aspx) to open the section, and use [IMAPIProp::GetProps](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) to get the property values.</span></span>  <br/> |
|[<span data-ttu-id="5f5fe-139">目次テーブル</span><span class="sxs-lookup"><span data-stu-id="5f5fe-139">Contents Tables</span></span>](https://msdn.microsoft.com/library/7b8efb4e-b5be-41b8-81bb-9aa1da421433%28Office.15%29.aspx) <br/> |<span data-ttu-id="5f5fe-140">メッセージストアプロバイダーは、フォルダーのコンテンツテーブルを実装します。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-140">Message store providers implement contents tables for their folders.</span></span> <span data-ttu-id="5f5fe-141">フォルダーの関連部分に含まれる非表示のメッセージの場合、メッセージストアプロバイダーは関連付けられたコンテンツテーブルをサポートし、クライアントは[IMAPIContainer:: getcontentstable](https://msdn.microsoft.com/library/88c7a666-875d-473a-b126-dbbb7009f7d9%28Office.15%29.aspx)メソッドを使用して、関連付けられた contents テーブルへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-141">For hidden messages in the associated part of a folder, message store providers support associated contents tables, and clients can use the [IMAPIContainer::GetContentsTable](https://msdn.microsoft.com/library/88c7a666-875d-473a-b126-dbbb7009f7d9%28Office.15%29.aspx) method to return a pointer to the associated contents table.</span></span>  <br/> |
|[<span data-ttu-id="5f5fe-142">制限について</span><span class="sxs-lookup"><span data-stu-id="5f5fe-142">About Restrictions</span></span>](https://msdn.microsoft.com/library/e119fa20-08b8-4c8d-93fc-56037220890d%28Office.15%29.aspx) <br/> [<span data-ttu-id="5f5fe-143">制限の種類</span><span class="sxs-lookup"><span data-stu-id="5f5fe-143">Types of Restrictions</span></span>](https://msdn.microsoft.com/library/0d3bd58b-7100-4117-91ac-27139715c85b%28Office.15%29.aspx) <br/> [<span data-ttu-id="5f5fe-144">制限の作成</span><span class="sxs-lookup"><span data-stu-id="5f5fe-144">Building a Restriction</span></span>](https://msdn.microsoft.com/library/12abbd8c-f825-493e-af42-344371d9658e%28Office.15%29.aspx) <br/> [<span data-ttu-id="5f5fe-145">制限コードの例</span><span class="sxs-lookup"><span data-stu-id="5f5fe-145">Sample Restriction Code</span></span>](https://msdn.microsoft.com/library/9b82097c-dbd6-4ba0-a6cb-292301f9402b%28Office.15%29.aspx) <br/> |<span data-ttu-id="5f5fe-146">MAPI では、クライアントは、コンテンツテーブルのフィルター処理に制限を使用して、特定のプロパティが特定の値に設定されているメッセージを表す行を検索できます。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-146">In MAPI, clients can use restrictions to filter contents tables, to search for rows that represent messages that have a certain property set to a specific value.</span></span> <span data-ttu-id="5f5fe-147">制限は、 [srestriction](https://msdn.microsoft.com/library/c12b4409-da6f-480b-87af-1e5baea2e8bd%28Office.15%29.aspx)データ構造を使用して定義されます。これには、さらに特殊な制限構造の和集合を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-147">Restrictions are defined by using the [SRestriction](https://msdn.microsoft.com/library/c12b4409-da6f-480b-87af-1e5baea2e8bd%28Office.15%29.aspx) data structure, which can contain a union of more specialized restriction structures.</span></span> <span data-ttu-id="5f5fe-148">[IMAPITable:: FindRow](https://msdn.microsoft.com/library/6511368c-9777-497e-9eea-cf390c04b92e%28Office.15%29.aspx)メソッドは、制限を適用し、制限条件に一致するテーブルの最初の行を取得します。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-148">The [IMAPITable::FindRow](https://msdn.microsoft.com/library/6511368c-9777-497e-9eea-cf390c04b92e%28Office.15%29.aspx) method applies a restriction and retrieves the first row in a table that matches the restriction criteria.</span></span>  <br/> |
|[<span data-ttu-id="5f5fe-149">インデックス作成のためのストア登録について</span><span class="sxs-lookup"><span data-stu-id="5f5fe-149">About Registering Stores for Indexing</span></span>](https://msdn.microsoft.com/library/dd2aa06a-96e8-1291-18b5-fc3c40b74e4d%28Office.15%29.aspx) <br/> |<span data-ttu-id="5f5fe-150">[PidTagStoreProvider](https://msdn.microsoft.com/library/6f6cc66f-a08e-4f8e-b33a-d3674319248e%28Office.15%29.aspx) (**PR_MDB_PROVIDER**) プロパティを使用して、ストアプロバイダーの種類を確認します。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-150">Use the [PidTagStoreProvider](https://msdn.microsoft.com/library/6f6cc66f-a08e-4f8e-b33a-d3674319248e%28Office.15%29.aspx) (**PR_MDB_PROVIDER**) property to verify the type of store provider.</span></span> <span data-ttu-id="5f5fe-151">たとえば、ストアが Exchange ストアであるかどうかを確認するには、 **PidTagStoreProvider**プロパティは、パブリックヘッダーファイル edkmdb で定義されている定数**pbexchangeproviderprimaryuserguid**で表される値を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-151">For example, to verify whether a store is an Exchange store, the **PidTagStoreProvider** property should return a value represented by the constant **pbExchangeProviderPrimaryUserGuid**, which is defined in the public header file edkmdb.h.</span></span>  <br/> |
   
## <a name="locating-the-appropriate-hidden-message-and-attachment"></a><span data-ttu-id="5f5fe-152">適切な非表示メッセージと添付ファイルを特定する</span><span class="sxs-lookup"><span data-stu-id="5f5fe-152">Locating the appropriate hidden message and attachment</span></span>

<span data-ttu-id="5f5fe-153">受信トレイのメッセージのダウンロード履歴が非表示メッセージへの添付ファイルの**PidTagAttachDataBinary**プロパティに含まれていることがわかったので、該当する非表示メッセージの適切な添付ファイルを特定するには、次の手順を実行します。ここ</span><span class="sxs-lookup"><span data-stu-id="5f5fe-153">Now that we know the message download history for an Inbox is in the **PidTagAttachDataBinary** property of an attachment to a hidden message, the procedure to locate the appropriate attachment of the appropriate hidden message involves the following procedures:</span></span> 
  
1. [<span data-ttu-id="5f5fe-154">適切な非表示メッセージを見つける</span><span class="sxs-lookup"><span data-stu-id="5f5fe-154">Find the appropriate hidden message</span></span>](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindHiddenMsg)
    
2. [<span data-ttu-id="5f5fe-155">非表示メッセージの適切な添付ファイルを検索する</span><span class="sxs-lookup"><span data-stu-id="5f5fe-155">Find the appropriate attachment of the hidden message</span></span>](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindAttachment)
    
3. [<span data-ttu-id="5f5fe-156">メッセージの添付ファイルの PidTagAttachDataBinary プロパティにアクセスする</span><span class="sxs-lookup"><span data-stu-id="5f5fe-156">Access the PidTagAttachDataBinary property of the message attachment</span></span>](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_AccessProp)

<span data-ttu-id="5f5fe-157"><a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindHiddenMsg"> </a></span><span class="sxs-lookup"><span data-stu-id="5f5fe-157"></span></span>

### <a name="find-the-appropriate-hidden-message"></a><span data-ttu-id="5f5fe-158">適切な非表示メッセージを見つける</span><span class="sxs-lookup"><span data-stu-id="5f5fe-158">Find the appropriate hidden message</span></span>

1. <span data-ttu-id="5f5fe-159">プロファイルから、 **MUID_PROFILE_INSTANCE**で指定されたプロファイルセクションの[PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) (**PR_SEARCH_KEY**) プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-159">Get the [PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) (**PR_SEARCH_KEY**) property from the profile, in the profile section specified by **MUID_PROFILE_INSTANCE**.</span></span>
    
2. <span data-ttu-id="5f5fe-160">**IMAPIContainer:: getcontentstable**を呼び出して、受信トレイフォルダーに関連付けられているコンテンツを開きます。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-160">Open the Associated Contents for the Inbox folder by calling **IMAPIContainer::GetContentsTable**.</span></span>
    
3. <span data-ttu-id="5f5fe-161">[PidTagConversationKey](https://msdn.microsoft.com/library/52c97d6c-7f4b-4522-aeac-0c1ed8475952%28Office.15%29.aspx) (**PR_CONVERSATION_KEY**)、 **PidTagSearchKey** (**PR_SEARCH_KEY**)、および[PidTagMessageClass](https://msdn.microsoft.com/library/1e704023-1992-4b43-857e-0a7da7bc8e87%28Office.15%29.aspx) (**PR_MESSAGE_CLASS**) の各プロパティに基づいて制限を作成し、テーブルを取得します。受信トレイの関連コンテンツのすべての非表示メッセージを含みます。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-161">Create a restriction based on the [PidTagConversationKey](https://msdn.microsoft.com/library/52c97d6c-7f4b-4522-aeac-0c1ed8475952%28Office.15%29.aspx) (**PR_CONVERSATION_KEY**), **PidTagSearchKey** (**PR_SEARCH_KEY**), and [PidTagMessageClass](https://msdn.microsoft.com/library/1e704023-1992-4b43-857e-0a7da7bc8e87%28Office.15%29.aspx) (**PR_MESSAGE_CLASS**) properties to get a table that contains all the hidden messages in the Associated Contents of the Inbox.</span></span> <span data-ttu-id="5f5fe-162">次に示すのは、 [POP3 UIDL 履歴の検索](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/03/locating-the-pop3-uidl-history.aspx)から抽出される制限の例です。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-162">The following is an example of a restriction extracted from [Locating the POP3 UIDL History](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/03/locating-the-pop3-uidl-history.aspx).</span></span>
    
   ```cpp
      SRestriction rgRes[3]; 
      SPropValue rgProps[3]; 
      rgRes[0].rt = RES_AND; 
      rgRes[0].res.resAnd.cRes = 2; 
      rgRes[0].res.resAnd.lpRes = &amp;rgRes[1]; 
      rgRes[1].rt = RES_PROPERTY; 
      rgRes[1].res.resProperty.relop = RELOP_EQ; 
      rgRes[1].res.resProperty.ulPropTag = PR_CONVERSATION_KEY; 
      rgRes[1].res.resProperty.lpProp = &amp;rgProps[0]; 
      rgRes[2].rt = RES_PROPERTY; 
      rgRes[2].res.resProperty.relop = RELOP_EQ; 
      rgRes[2].res.resProperty.ulPropTag = PR_MESSAGE_CLASS; 
      rgRes[2].res.resProperty.lpProp = &amp;rgProps[1]; 
      rgProps[0].ulPropTag = PR_CONVERSATION_KEY; 
      rgProps[0].Value.bin = pVals[iSearchKey].Value.bin; // PR_SEARCH_KEY from the profile 
      rgProps[1].ulPropTag = PR_MESSAGE_CLASS; 
      rgProps[1].Value.LPSZ = (LPTSTR)"IPM.MessageManager";
   ```

4. <span data-ttu-id="5f5fe-163">表から、 **IMAPITable:: FindRow**を使用して隠しメッセージを検索します。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-163">From the table, find the hidden message by using **IMAPITable::FindRow**.</span></span>
    
5. <span data-ttu-id="5f5fe-164">非表示メッセージの検索に失敗した場合は、次のように、 **PidTagSearchKey** (**PR_SEARCH_KEY**) を**PidTagConversationKey**の代わりに使用するように制限を変更します。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-164">If step 4 fails to find a hidden message, change the restriction to use **PidTagSearchKey** (**PR_SEARCH_KEY**) instead of **PidTagConversationKey**, as shown below:</span></span>
    
   ```cpp
    rgRes[1].res.resProperty.ulPropTag = rgProps[0].ulPropTag = PR_SEARCH_KEY;
   ```

6. <span data-ttu-id="5f5fe-165">**IMAPITable:: FindRow**を使用して、隠しメッセージを検索します。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-165">Find the hidden message using **IMAPITable::FindRow**.</span></span> 
    
7. <span data-ttu-id="5f5fe-166">手順6でエラーが発生した場合は、 [PidTagSubject](https://msdn.microsoft.com/library/aa7ba4d9-c5e0-4ce7-a34e-65f675223bc9%28Office.15%29.aspx) (**PR_SUBJECT**) を使用するように制限を変更し`printf` 、次の値と等しくなるようにします (以下にスタイル置換を使用して簡潔に説明します)。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-166">If Step 6 fails, change the restriction to use [PidTagSubject](https://msdn.microsoft.com/library/aa7ba4d9-c5e0-4ce7-a34e-65f675223bc9%28Office.15%29.aspx) (**PR_SUBJECT**) being equal to the following value (shown below using  `printf` style substitution for brevity).</span></span> 
    
   ```cpp
    "Outlook Message Manager (%s) (KEY: %s)", PR_PROFILE_NAME, HexFromBin(PR_SEARCH_KEY)
   ```

8. <span data-ttu-id="5f5fe-167">**IMAPITable:: FindRow**を使用して、隠しメッセージを検索します。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-167">Find the hidden message by using **IMAPITable::FindRow**.</span></span>
    
9. <span data-ttu-id="5f5fe-168">Outlook 2010 またはそれ以降のバージョンを実行している場合は、 **PidTagProfileName** (**PR_PROFILE_NAME**) および**PidTagSearchKey** (**PR_SEARCH_KEY**) にそれぞれ次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-168">If you are running Outlook 2010 or a later version, use the following values for **PidTagProfileName** (**PR_PROFILE_NAME**) and **PidTagSearchKey** (**PR_SEARCH_KEY**), respectively.</span></span>
    
   ```cpp
    CHAR g_szGeneralKey[] = "General Key"; 
    const SBinary g_binGeneralKey = {sizeof(g_szGeneralKey), (LPBYTE)g_szGeneralKey};
   ```

   <span data-ttu-id="5f5fe-169">手順 3 ~ 8 を実行します。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-169">Run through Steps 3 through 8.</span></span> <span data-ttu-id="5f5fe-170">これでメッセージの検索に失敗した場合は、元の手順 3 ~ 8 に戻ります。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-170">If this fails to find a message, fall back to the original steps 3 through 8.</span></span>
    
10. <span data-ttu-id="5f5fe-171">手順4、6、または8で見つかった非表示のメッセージを開きます。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-171">Open the hidden message found in Step 4, 6, or 8.</span></span>

<span data-ttu-id="5f5fe-172"><a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindAttachment"> </a></span><span class="sxs-lookup"><span data-stu-id="5f5fe-172"></span></span>

### <a name="find-the-appropriate-attachment-of-the-hidden-message"></a><span data-ttu-id="5f5fe-173">非表示メッセージの適切な添付ファイルを検索する</span><span class="sxs-lookup"><span data-stu-id="5f5fe-173">Find the appropriate attachment of the hidden message</span></span>

<span data-ttu-id="5f5fe-174">非表示のメッセージには複数の添付ファイルがある場合があるので、次の順序で該当する添付ファイルを探します。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-174">Because the hidden message may have more than one attachment, look for the appropriate attachment in the following order.</span></span>
  
> [!NOTE]
> <span data-ttu-id="5f5fe-175">この手順を実行する`printf`と、簡潔にするためにスタイルの代替が使用されます。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-175">This procedure again uses the  `printf` style substitution for brevity.</span></span> 

1. <span data-ttu-id="5f5fe-176">[PidTagAttachLongFilename](https://msdn.microsoft.com/library/83b69e8f-0b5a-4992-b5b8-160d3bdfa22a%28Office.15%29.aspx) (**PR_ATTACH_LONG_FILENAME**) が次の文字列と一致する添付ファイルを検索`szEmailAddress`します。ここで、はユーザーのプロファイルに指定されたユーザーの SMTP アドレスです。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-176">Look for an attachment whose [PidTagAttachLongFilename](https://msdn.microsoft.com/library/83b69e8f-0b5a-4992-b5b8-160d3bdfa22a%28Office.15%29.aspx) (**PR_ATTACH_LONG_FILENAME**) matches the following string, where  `szEmailAddress` is the user's SMTP address, as specified in the user's profile.</span></span> <span data-ttu-id="5f5fe-177">.</span><span class="sxs-lookup"><span data-stu-id="5f5fe-177"></span></span> 
    
   ```cpp
    "BlobPOP%s", szEmailAddress
   ```

2. <span data-ttu-id="5f5fe-178">[PidTagAttachFilename](https://msdn.microsoft.com/library/cbf34dd6-7733-47f6-9c41-9d82656ca9dc%28Office.15%29.aspx) (**PR_ATTACH_FILENAME**) が "blobpop% s" と一致する添付ファイルを`szEmailAddress`探します。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-178">Look for an attachment whose [PidTagAttachFilename](https://msdn.microsoft.com/library/cbf34dd6-7733-47f6-9c41-9d82656ca9dc%28Office.15%29.aspx) (**PR_ATTACH_FILENAME**) matches "BlobPOP%s",  `szEmailAddress`.</span></span>
    
3. <span data-ttu-id="5f5fe-179">[PidTagDisplayName](https://msdn.microsoft.com/library/bd094e00-5c60-4bb3-9a45-b943fab52876%28Office.15%29.aspx) (**PR_DISPLAY_NAME**) が "blobpop% s" と一致する添付ファイルを`szEmailAddress`探します。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-179">Look for an attachment whose [PidTagDisplayName](https://msdn.microsoft.com/library/bd094e00-5c60-4bb3-9a45-b943fab52876%28Office.15%29.aspx) (**PR_DISPLAY_NAME**) matches "BlobPOP%s",  `szEmailAddress`.</span></span>
    
4. <span data-ttu-id="5f5fe-180">**PidTagAttachFilename** (**PR_ATTACH_FILENAME**) が "Blob% .8x" `dwAcctUID`と一致する添付ファイルを検索します`dwAcctUID` 。ここで、は[PROP_ACCT_MINI_UID](prop_acct_mini_uid.md)からのものです。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-180">Look for an attachment whose **PidTagAttachFilename** (**PR_ATTACH_FILENAME**) matches "Blob%.8x",  `dwAcctUID`, where  `dwAcctUID` comes from [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md).</span></span> <span data-ttu-id="5f5fe-181">**PROP_ACCT_MINI_UID**プロパティにアクセスするには、 [IOlkAccount:: getprop](iolkaccount-getprop.md)メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-181">You can use the [IOlkAccount::GetProp](iolkaccount-getprop.md) method to access the **PROP_ACCT_MINI_UID** property.</span></span> 

<span data-ttu-id="5f5fe-182"><a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_AccessProp"> </a></span><span class="sxs-lookup"><span data-stu-id="5f5fe-182"></span></span>

### <a name="access-the-pidtagattachdatabinary-property-of-the-message-attachment"></a><span data-ttu-id="5f5fe-183">メッセージの添付ファイルの PidTagAttachDataBinary プロパティにアクセスする</span><span class="sxs-lookup"><span data-stu-id="5f5fe-183">Access the PidTagAttachDataBinary property of the message attachment</span></span>

<span data-ttu-id="5f5fe-184">非表示メッセージの適切なメッセージ添付ファイルを特定した後、 **imapiprop:: GetProps**を使用して添付ファイルの**PidTagAttachDataBinary**プロパティを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-184">After locating the appropriate message attachment of the hidden message, use **IMAPIProp::GetProps** to read the **PidTagAttachDataBinary** property of the attachment.</span></span> 

<span data-ttu-id="5f5fe-185"><a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_NextSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="5f5fe-185"></span></span>

## <a name="next-steps"></a><span data-ttu-id="5f5fe-186">次の手順</span><span class="sxs-lookup"><span data-stu-id="5f5fe-186">Next steps</span></span>

<span data-ttu-id="5f5fe-187">このトピックでは、POP3 メールクライアントの受信トレイのメッセージダウンロード履歴を見つける方法について説明しました。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-187">You have learned from this topic how to locate the message download history for the Inbox of a POP3 mail client.</span></span> <span data-ttu-id="5f5fe-188">この履歴を解析して、受信トレイでダウンロードまたは削除されたメッセージを識別する方法については、「 [POP3 アカウントのメッセージダウンロード履歴の解析](parsing-the-message-download-history-for-a-pop3-account.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5f5fe-188">See [Parsing the message download history for a POP3 account](parsing-the-message-download-history-for-a-pop3-account.md) to learn how to parse this history to identify messages that have been downloaded or deleted for the Inbox.</span></span> 

<span data-ttu-id="5f5fe-189"><a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_AdditionalRsc"> </a></span><span class="sxs-lookup"><span data-stu-id="5f5fe-189"></span></span>

## <a name="see-also"></a><span data-ttu-id="5f5fe-190">関連項目</span><span class="sxs-lookup"><span data-stu-id="5f5fe-190">See also</span></span>

- [<span data-ttu-id="5f5fe-191">POP3 アカウントのメッセージ ダウンロードの管理</span><span class="sxs-lookup"><span data-stu-id="5f5fe-191">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md)   
- [<span data-ttu-id="5f5fe-192">POP3 アカウントのメッセージのダウンロードの履歴の解析</span><span class="sxs-lookup"><span data-stu-id="5f5fe-192">Parsing the message download history for a POP3 account</span></span>](parsing-the-message-download-history-for-a-pop3-account.md)
- [<span data-ttu-id="5f5fe-193">POP3 の UIDL の履歴を見つける</span><span class="sxs-lookup"><span data-stu-id="5f5fe-193">Locating the POP3 UIDL History</span></span>](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/03/locating-the-pop3-uidl-history.aspx)
    

