---
title: 会議の更新のオプションのプロパティを非表示にします。
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 25942df6f6156266f16cf6e681270dbb530472e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800207"
---
# <a name="hide-meeting-update-option-property"></a><span data-ttu-id="3440f-103">会議の更新のオプションのプロパティを非表示にします。</span><span class="sxs-lookup"><span data-stu-id="3440f-103">Hide Meeting Update Option Property</span></span>

  
  
<span data-ttu-id="3440f-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3440f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3440f-105">のみ追加または削除された出席者に会議の更新を送信するオプションを非表示にします。</span><span class="sxs-lookup"><span data-stu-id="3440f-105">Hides the option to send meeting updates to only added or deleted attendees.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="3440f-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="3440f-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3440f-107">公開されます。</span><span class="sxs-lookup"><span data-stu-id="3440f-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="3440f-108">[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)オブジェクト</span><span class="sxs-lookup"><span data-stu-id="3440f-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="3440f-109">によって作成されます。</span><span class="sxs-lookup"><span data-stu-id="3440f-109">Created by:</span></span>  <br/> |<span data-ttu-id="3440f-110">ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="3440f-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="3440f-111">によってアクセスします。</span><span class="sxs-lookup"><span data-stu-id="3440f-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="3440f-112">Outlook およびその他のクライアント</span><span class="sxs-lookup"><span data-stu-id="3440f-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="3440f-113">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="3440f-113">Property type:</span></span>  <br/> |<span data-ttu-id="3440f-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="3440f-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="3440f-115">アクセスの種類:</span><span class="sxs-lookup"><span data-stu-id="3440f-115">Access type:</span></span>  <br/> |<span data-ttu-id="3440f-116">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="3440f-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3440f-117">備考</span><span class="sxs-lookup"><span data-stu-id="3440f-117">Remarks</span></span>

<span data-ttu-id="3440f-118">ストア機能を提供するストア プロバイダーを実装する必要があります[IMAPIProp: IUnknown](imapipropiunknown.md) 、 [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)の呼び出しに渡されたこれらのプロパティのいずれかのプロパティの有効なタグを返すとします。</span><span class="sxs-lookup"><span data-stu-id="3440f-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="3440f-119">これらのプロパティのいずれかのプロパティ タグが[IMAPIProp::GetProps](imapiprop-getprops.md)に渡されると、ストア プロバイダーを使用、正しいプロパティ値を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="3440f-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="3440f-120">ストア プロバイダーには、取得、またはこれらのプロパティを設定するには、 [HrGetOneProp](hrgetoneprop.md)と[HrSetOneProp](hrsetoneprop.md)を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="3440f-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="3440f-121">このプロパティの値を取得するには、クライアントはまず[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)を使用して、プロパティ タグを取得して、値を取得する[IMAPIProp::GetProps](imapiprop-getprops.md)でこのプロパティのタグを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3440f-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="3440f-122">[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)を呼び出すときは、 _lppPropNames_の入力パラメーターで示される[MAPINAMEID](mapinameid.md)構造体の次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="3440f-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3440f-123">lpGuid。</span><span class="sxs-lookup"><span data-stu-id="3440f-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="3440f-124">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="3440f-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="3440f-125">ulKind。</span><span class="sxs-lookup"><span data-stu-id="3440f-125">ulKind:</span></span>  <br/> |<span data-ttu-id="3440f-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="3440f-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="3440f-127">Kind.lpwstrName。</span><span class="sxs-lookup"><span data-stu-id="3440f-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="3440f-128">L"urn: スキーマ-マイクロソフト-com:office:outlook #allornonemtgupdatedlg」</span><span class="sxs-lookup"><span data-stu-id="3440f-128">L"urn:schemas-microsoft-com:office:outlook#allornonemtgupdatedlg"</span></span>  <br/> |
   
<span data-ttu-id="3440f-129">ストア プロバイダー、サーバーを使用して、会議の更新を送信するには、**出席者に更新内容を送信**] ダイアログ ボックスで変更できます。</span><span class="sxs-lookup"><span data-stu-id="3440f-129">A store provider that uses a server to send meeting updates can modify the **Send Update to Attendees** dialog box.</span></span> <span data-ttu-id="3440f-130">どの参加者が追加されたり、最初の会議出席依頼した後にユーザーが削除サーバーでは、会議の更新を送信するとき、サーバーは認識できないために、この機能の使用をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="3440f-130">This functionality is useful because when the server sends a meeting update, the server does not know which attendees have been added or deleted by the user since the initial meeting request.</span></span> <span data-ttu-id="3440f-131">このプロパティが**true**の場合、**出席者に更新を送信**] ダイアログ ボックスで**追加または削除された出席者にのみ更新を送信**する] オプションは表示されません。</span><span class="sxs-lookup"><span data-stu-id="3440f-131">When this property is **true**, the **Send update only to added or deleted attendees** option is not displayed in the **Send Update to Attendees** dialog box.</span></span> 
  
<span data-ttu-id="3440f-132">Outlook のバージョンの Microsoft Office Outlook 2003 Service Pack 1 より前の場合、またはその値が**false**の場合、このプロパティは無視されます。</span><span class="sxs-lookup"><span data-stu-id="3440f-132">This property is ignored if the version of Outlook is earlier than Microsoft Office Outlook 2003 Service Pack 1, or if its value is **false**.</span></span>
  

