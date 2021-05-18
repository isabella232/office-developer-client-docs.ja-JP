---
title: 会議の更新オプションプロパティを非表示にする
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Hide Meeting Update Option Property
api_type:
- COM
ms.assetid: 9e7b413f-a88a-a4ec-8d57-1f3058cce4a4
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ac7c891fa05560231a257f9bd52ccbbfe564b49d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412101"
---
# <a name="hide-meeting-update-option-property"></a><span data-ttu-id="10bce-103">会議の更新オプションプロパティを非表示にする</span><span class="sxs-lookup"><span data-stu-id="10bce-103">Hide Meeting Update Option Property</span></span>

  
  
<span data-ttu-id="10bce-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="10bce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="10bce-105">追加または削除された出席者にのみ会議の更新プログラムを送信するオプションを非表示にします。</span><span class="sxs-lookup"><span data-stu-id="10bce-105">Hides the option to send meeting updates to only added or deleted attendees.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="10bce-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="10bce-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="10bce-107">次の場合に公開されます。</span><span class="sxs-lookup"><span data-stu-id="10bce-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="10bce-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) オブジェクト</span><span class="sxs-lookup"><span data-stu-id="10bce-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="10bce-109">作成者:</span><span class="sxs-lookup"><span data-stu-id="10bce-109">Created by:</span></span>  <br/> |<span data-ttu-id="10bce-110">ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="10bce-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="10bce-111">アクセス者:</span><span class="sxs-lookup"><span data-stu-id="10bce-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="10bce-112">Outlookクライアント</span><span class="sxs-lookup"><span data-stu-id="10bce-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="10bce-113">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="10bce-113">Property type:</span></span>  <br/> |<span data-ttu-id="10bce-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="10bce-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="10bce-115">アクセスの種類:</span><span class="sxs-lookup"><span data-stu-id="10bce-115">Access type:</span></span>  <br/> |<span data-ttu-id="10bce-116">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="10bce-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="10bce-117">注釈</span><span class="sxs-lookup"><span data-stu-id="10bce-117">Remarks</span></span>

<span data-ttu-id="10bce-118">ストア機能を提供するには、ストア プロバイダーが [IMAPIProp : IUnknown](imapipropiunknown.md) を実装し [、IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) 呼び出しに渡されるこれらのプロパティの有効なプロパティ タグを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="10bce-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="10bce-119">これらのプロパティのプロパティ タグが [IMAPIProp::GetProps](imapiprop-getprops.md)に渡される場合、ストア プロバイダーは正しいプロパティ値も返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="10bce-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="10bce-120">ストア プロバイダーは [、HrGetOneProp](hrgetoneprop.md) と [HrSetOneProp](hrsetoneprop.md) を呼び出して、これらのプロパティを取得または設定できます。</span><span class="sxs-lookup"><span data-stu-id="10bce-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="10bce-121">このプロパティの値を取得するには、まず [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) を使用してプロパティ タグを取得し [、IMAPIProp::GetProps](imapiprop-getprops.md) でこのプロパティ タグを指定して値を取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="10bce-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="10bce-122">[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)を呼び出す場合は、入力パラメーター _lppPropNames_ が指す [MAPINAMEID](mapinameid.md)構造体に次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="10bce-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="10bce-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="10bce-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="10bce-124">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="10bce-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="10bce-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="10bce-125">ulKind:</span></span>  <br/> |<span data-ttu-id="10bce-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="10bce-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="10bce-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="10bce-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="10bce-128">L"urn:schemas-microsoft-com:office:outlook#allornonemtgupdatedlg"</span><span class="sxs-lookup"><span data-stu-id="10bce-128">L"urn:schemas-microsoft-com:office:outlook#allornonemtgupdatedlg"</span></span>  <br/> |
   
<span data-ttu-id="10bce-129">サーバーを使用して会議の更新プログラムを送信するストア プロバイダーは、[出席者に更新プログラムを送信する] ダイアログ ボックス **を** 変更できます。</span><span class="sxs-lookup"><span data-stu-id="10bce-129">A store provider that uses a server to send meeting updates can modify the **Send Update to Attendees** dialog box.</span></span> <span data-ttu-id="10bce-130">この機能は、サーバーが会議の更新プログラムを送信するときに、最初の会議出席依頼以降にユーザーが追加または削除した出席者をサーバーが知らないので便利です。</span><span class="sxs-lookup"><span data-stu-id="10bce-130">This functionality is useful because when the server sends a meeting update, the server does not know which attendees have been added or deleted by the user since the initial meeting request.</span></span> <span data-ttu-id="10bce-131">このプロパティが **true の場合**、[更新プログラムを追加または削除した出席者にのみ送信する] オプションは、[出席者に更新プログラムを送信する] ダイアログ ボックス **には** 表示されません。</span><span class="sxs-lookup"><span data-stu-id="10bce-131">When this property is **true**, the **Send update only to added or deleted attendees** option is not displayed in the **Send Update to Attendees** dialog box.</span></span> 
  
<span data-ttu-id="10bce-132">このプロパティは、2003 Service Pack 1 のバージョンOutlook 2003 Service Pack 1 より前Microsoft Office Outlook、または値が false の場合は無視 **されます**。</span><span class="sxs-lookup"><span data-stu-id="10bce-132">This property is ignored if the version of Outlook is earlier than Microsoft Office Outlook 2003 Service Pack 1, or if its value is **false**.</span></span>
  

