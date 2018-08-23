---
title: すべてのメッセージの受信者プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 18c96796-f38d-4058-9c51-9c5a14990846
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d92e9dbbf594dffc3dbf5bbf271fc80a0abed68e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803718"
---
# <a name="recipient-properties-for-all-messages"></a><span data-ttu-id="cb26d-103">すべてのメッセージの受信者プロパティ</span><span class="sxs-lookup"><span data-stu-id="cb26d-103">Recipient Properties for All Messages</span></span>

  
  
<span data-ttu-id="cb26d-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cb26d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cb26d-105">次のプロパティは、通常、すべてのメッセージ受信者の存在です。</span><span class="sxs-lookup"><span data-stu-id="cb26d-105">The following properties are typically present for all message recipients.</span></span> <span data-ttu-id="cb26d-106">**PR_EMAIL_ADDRESS**と**PR_SEARCH_KEY**は省略可能です。すべての他のプロパティは、必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb26d-106">**PR_EMAIL_ADDRESS** and **PR_SEARCH_KEY** are optional; all of the other properties are required.</span></span> 
  
<span data-ttu-id="cb26d-107">**テーブルのタイトル**</span><span class="sxs-lookup"><span data-stu-id="cb26d-107">**Table Title**</span></span>

|<span data-ttu-id="cb26d-108">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="cb26d-108">**Property**</span></span>|<span data-ttu-id="cb26d-109">**説明**</span><span class="sxs-lookup"><span data-stu-id="cb26d-109">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cb26d-110">**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cb26d-110">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cb26d-111">SMTP など、メッセージング ユーザーの電子メール アドレスの種類が含まれています。</span><span class="sxs-lookup"><span data-stu-id="cb26d-111">Contains the messaging user's email address type, such as SMTP.</span></span>  <br/> |
|<span data-ttu-id="cb26d-112">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cb26d-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cb26d-113">特定の MAPI オブジェクトの表示名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="cb26d-113">Contains the display name for a given MAPI object.</span></span>  <br/> |
|<span data-ttu-id="cb26d-114">**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cb26d-114">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cb26d-115">テーブルの特定の行にアイコンを関連付けるに使用する値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="cb26d-115">Contains a value used to associate an icon with a particular row of a table.</span></span>  <br/> |
|<span data-ttu-id="cb26d-116">**PR_EMAIL_ADDRESS**([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cb26d-116">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cb26d-117">メッセージング ユーザーの電子メール アドレスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="cb26d-117">Contains the messaging user's email address.</span></span>  <br/> |
|<span data-ttu-id="cb26d-118">**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cb26d-118">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cb26d-119">開き、特定の MAPI オブジェクトのプロパティを編集するに使用される MAPI エントリの識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="cb26d-119">Contains a MAPI entry identifier used to open and edit properties of a particular MAPI object.</span></span>  <br/> |
|<span data-ttu-id="cb26d-120">**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cb26d-120">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cb26d-121">オブジェクトの種類が含まれています。</span><span class="sxs-lookup"><span data-stu-id="cb26d-121">Contains the type of an object.</span></span>  <br/> |
|<span data-ttu-id="cb26d-122">**PR_SEARCH_KEY**([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cb26d-122">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cb26d-123">検索の相関関係を持つオブジェクトを識別するバイナリの比較可能なキーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="cb26d-123">Contains a binary-comparable key that identifies correlated objects for a search.</span></span>  <br/> |
   

