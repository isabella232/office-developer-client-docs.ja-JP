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
ms.openlocfilehash: 3c5764d74039249ccac47d449f0ebd4042893434
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328442"
---
# <a name="recipient-properties-for-all-messages"></a><span data-ttu-id="0f097-103">すべてのメッセージの受信者プロパティ</span><span class="sxs-lookup"><span data-stu-id="0f097-103">Recipient Properties for All Messages</span></span>

  
  
<span data-ttu-id="0f097-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0f097-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0f097-105">通常、次のプロパティはすべてのメッセージの受信者に表示されます。</span><span class="sxs-lookup"><span data-stu-id="0f097-105">The following properties are typically present for all message recipients.</span></span> <span data-ttu-id="0f097-106">**PR_EMAIL_ADDRESS**および**PR_SEARCH_KEY**は省略可能です。その他のすべてのプロパティが必要です。</span><span class="sxs-lookup"><span data-stu-id="0f097-106">**PR_EMAIL_ADDRESS** and **PR_SEARCH_KEY** are optional; all of the other properties are required.</span></span> 
  
<span data-ttu-id="0f097-107">**表のタイトル**</span><span class="sxs-lookup"><span data-stu-id="0f097-107">**Table Title**</span></span>

|<span data-ttu-id="0f097-108">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="0f097-108">**Property**</span></span>|<span data-ttu-id="0f097-109">**説明**</span><span class="sxs-lookup"><span data-stu-id="0f097-109">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0f097-110">**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0f097-110">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0f097-111">メッセージングユーザーの電子メールアドレスの種類 (SMTP など) を格納します。</span><span class="sxs-lookup"><span data-stu-id="0f097-111">Contains the messaging user's email address type, such as SMTP.</span></span>  <br/> |
|<span data-ttu-id="0f097-112">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0f097-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0f097-113">指定した MAPI オブジェクトの表示名を格納します。</span><span class="sxs-lookup"><span data-stu-id="0f097-113">Contains the display name for a given MAPI object.</span></span>  <br/> |
|<span data-ttu-id="0f097-114">**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0f097-114">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0f097-115">表の特定の行にアイコンを関連付けるために使用される値を格納します。</span><span class="sxs-lookup"><span data-stu-id="0f097-115">Contains a value used to associate an icon with a particular row of a table.</span></span>  <br/> |
|<span data-ttu-id="0f097-116">**PR_EMAIL_ADDRESS**([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0f097-116">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0f097-117">メッセージングユーザーの電子メールアドレスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="0f097-117">Contains the messaging user's email address.</span></span>  <br/> |
|<span data-ttu-id="0f097-118">**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0f097-118">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0f097-119">特定の mapi オブジェクトのプロパティを開いて編集するために使用する mapi エントリ識別子を含みます。</span><span class="sxs-lookup"><span data-stu-id="0f097-119">Contains a MAPI entry identifier used to open and edit properties of a particular MAPI object.</span></span>  <br/> |
|<span data-ttu-id="0f097-120">**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0f097-120">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0f097-121">オブジェクトの種類を格納します。</span><span class="sxs-lookup"><span data-stu-id="0f097-121">Contains the type of an object.</span></span>  <br/> |
|<span data-ttu-id="0f097-122">**PR_SEARCH_KEY**([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0f097-122">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0f097-123">検索の相関オブジェクトを識別する2つの比較可能なキーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="0f097-123">Contains a binary-comparable key that identifies correlated objects for a search.</span></span>  <br/> |
   

