---
title: MAPI のプロパティの概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02e5b23f-1bdb-4fbf-a27d-e3301a359573
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 99887bab2b576e6e6c05414ee9daf1bd6e8d0463
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408328"
---
# <a name="mapi-property-overview"></a><span data-ttu-id="740d2-103">MAPI のプロパティの概要</span><span class="sxs-lookup"><span data-stu-id="740d2-103">MAPI Property Overview</span></span>

  
  
<span data-ttu-id="740d2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="740d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="740d2-105">プロパティは、MAPI オブジェクトの属性です。</span><span class="sxs-lookup"><span data-stu-id="740d2-105">A property is an attribute of a MAPI object.</span></span> <span data-ttu-id="740d2-106">プロパティは、メッセージの件名やメッセージング ユーザーのアドレスの種類など、オブジェクトに関する情報を記述します。</span><span class="sxs-lookup"><span data-stu-id="740d2-106">Properties describe something about the object, such as the subject line of a message or the address type of a messaging user.</span></span> <span data-ttu-id="740d2-107">MAPI は、多くのプロパティを定義します。多くのオブジェクトを記述するプロパティと、特定の種類のオブジェクトにのみ適したプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="740d2-107">MAPI defines many properties, some to describe many objects and some that are appropriate only for an object of a particular type.</span></span> <span data-ttu-id="740d2-108">クライアントとサービス プロバイダーは、新しいカスタム プロパティを作成することで、MAPI の定義済みプロパティのセットを拡張できます。</span><span class="sxs-lookup"><span data-stu-id="740d2-108">Clients and service providers can extend MAPI's set of predefined properties by creating new, custom properties.</span></span> <span data-ttu-id="740d2-109">クライアントは、新しいメッセージ クラスを記述するプロパティを定義し、サービス プロバイダーは、メッセージング システムの一意の機能を公開するプロパティを定義できます。</span><span class="sxs-lookup"><span data-stu-id="740d2-109">Clients can define properties to describe new message classes, and service providers can define properties to expose the unique features of their messaging system.</span></span>
  
<span data-ttu-id="740d2-110">プロパティは、永続的または一時的な場合があります。</span><span class="sxs-lookup"><span data-stu-id="740d2-110">Properties can be persistent or temporary.</span></span> <span data-ttu-id="740d2-111">セッションからセッションに保持されるプロパティは、オブジェクトのデータまたはプロファイルに格納できます。</span><span class="sxs-lookup"><span data-stu-id="740d2-111">Properties that persist from session to session can be stored with their objects' data or in the profile.</span></span> <span data-ttu-id="740d2-112">一時プロパティは、現在のセッションの期間中のみ存在します。</span><span class="sxs-lookup"><span data-stu-id="740d2-112">Temporary properties exist only for the duration of the current session.</span></span> 
  
<span data-ttu-id="740d2-113">クライアントとサービス プロバイダーは、テーブルまたはプロパティ シートを持つユーザーにプロパティを表示できます。</span><span class="sxs-lookup"><span data-stu-id="740d2-113">Clients and service providers can show properties to users with either a table or a property sheet.</span></span> <span data-ttu-id="740d2-114">テーブルは、複数のオブジェクトに属する一部のプロパティの読み取り専用ビューをユーザーに提供します。</span><span class="sxs-lookup"><span data-stu-id="740d2-114">Tables provide users with a read-only view of some of the properties belonging to multiple objects.</span></span> <span data-ttu-id="740d2-115">データは行と列の形式で表示され、各行はオブジェクトを表し、各列はプロパティを表します。</span><span class="sxs-lookup"><span data-stu-id="740d2-115">The data is displayed in row and column format, with each row representing an object and each column a property.</span></span> <span data-ttu-id="740d2-116">プロパティ シートは、1 つのオブジェクトの関連プロパティを表示するタブ付きダイアログ ボックスです。</span><span class="sxs-lookup"><span data-stu-id="740d2-116">Property sheets are tabbed dialog boxes that display related properties for a single object.</span></span> <span data-ttu-id="740d2-117">プロパティ シートは、データへの読み取り専用または読み取り/書き込みアクセスを提供できます。</span><span class="sxs-lookup"><span data-stu-id="740d2-117">Property sheets can provide read-only or read/write access to the data.</span></span> <span data-ttu-id="740d2-118">ユーザーが変更を許可するかどうかは、プロパティ シートの実装者です。</span><span class="sxs-lookup"><span data-stu-id="740d2-118">Whether or not a user is allowed to make changes is up to the implementer of the property sheet.</span></span>
  
<span data-ttu-id="740d2-119">[IMAPIProp インターフェイス](imapipropiunknown.md)は、プロパティを操作する主なインターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="740d2-119">The [IMAPIProp](imapipropiunknown.md) interface is the primary interface for working with properties.</span></span> <span data-ttu-id="740d2-120">プロパティをサポートするオブジェクトはすべて **IMAPIProp を実装します**。</span><span class="sxs-lookup"><span data-stu-id="740d2-120">All objects that support properties implement **IMAPIProp**.</span></span> <span data-ttu-id="740d2-121">**IMAPIProp** には、プロパティ値の取得、プロパティのコピー、変更の実行と変更の保存、プロパティ名と識別子間のマッピング、および以前のエラーに関する情報の取得を行うメソッドが含まれます。</span><span class="sxs-lookup"><span data-stu-id="740d2-121">**IMAPIProp** includes methods for retrieving property values, copying properties, making changes and saving those changes, mapping between property names and their identifiers, and retrieving information about a prior error.</span></span> 
  
<span data-ttu-id="740d2-122">プロパティとプロパティに関する情報を記述するためのいくつかのデータ構造があります。</span><span class="sxs-lookup"><span data-stu-id="740d2-122">There are several data structures for describing properties and information about properties.</span></span> <span data-ttu-id="740d2-123">最も一般的に使用される構造体は [、SPropValue](spropvalue.md) 構造体と [SPropTagArray](sproptagarray.md) 構造体です。</span><span class="sxs-lookup"><span data-stu-id="740d2-123">The most commonly used structures are the [SPropValue](spropvalue.md) structure and the [SPropTagArray](sproptagarray.md) structure.</span></span> <span data-ttu-id="740d2-124">**SPropValue** 構造体には、プロパティを記述する 3 つの情報が含まれる。</span><span class="sxs-lookup"><span data-stu-id="740d2-124">The **SPropValue** structure contains the three pieces of information that describe a property:</span></span> 
  
- <span data-ttu-id="740d2-125">プロパティのデータまたは値。</span><span class="sxs-lookup"><span data-stu-id="740d2-125">Data, or value, of the property.</span></span>
    
- <span data-ttu-id="740d2-126">プロパティの値のデータ型 (整数やブール値など)。</span><span class="sxs-lookup"><span data-stu-id="740d2-126">Data type of the property's value, such as integer or Boolean.</span></span> 
    
- <span data-ttu-id="740d2-127">管理を担当するプロパティとコンポーネントを一意に識別する、特定の範囲内の数値。</span><span class="sxs-lookup"><span data-stu-id="740d2-127">Numeric value within a particular range that uniquely identify the property and component responsible for maintaining it.</span></span> <span data-ttu-id="740d2-128">たとえば、MAPI で定義されたメッセージ コンテンツ プロパティを保持する範囲と、カスタム メッセージ クラスのクライアントによって定義されたメッセージ コンテンツ プロパティを保持する別の範囲があります。</span><span class="sxs-lookup"><span data-stu-id="740d2-128">For example, there is a range to hold message content properties defined by MAPI and another range to hold message content properties defined by a client for a custom message class.</span></span> 
    
<span data-ttu-id="740d2-129">プロパティの種類と識別子は、プロパティ タグと呼ばれる 1 つのコンポーネントに結合されます。</span><span class="sxs-lookup"><span data-stu-id="740d2-129">The property type and identifier are combined into a single component called the property tag.</span></span> <span data-ttu-id="740d2-130">プロパティ タグは、プロパティを簡単に参照するために使用できる定数です。</span><span class="sxs-lookup"><span data-stu-id="740d2-130">Property tags are constants that can be used to easily refer to the property.</span></span> <span data-ttu-id="740d2-131">MAPI で定義されたプロパティのプロパティ タグは、MAPITAGS に含まれています。H ヘッダー ファイルと **SPropValue** 構造体の **ulPropTag メンバー** 。</span><span class="sxs-lookup"><span data-stu-id="740d2-131">Property tags for properties defined by MAPI are included in the MAPITAGS.H header file and in the **ulPropTag** member of an **SPropValue** structure.</span></span> <span data-ttu-id="740d2-132">クライアントとサービス プロバイダーは、プロパティ タグを使用して、対応するプロパティを識別、取得、および更新します。</span><span class="sxs-lookup"><span data-stu-id="740d2-132">Clients and service providers use property tags to identify, retrieve, and update the corresponding properties.</span></span> 
  
<span data-ttu-id="740d2-133">**SPropTagArray** 構造体は、プロパティ タグのカウントされた配列です。</span><span class="sxs-lookup"><span data-stu-id="740d2-133">The **SPropTagArray** structure is a counted array of property tags.</span></span> <span data-ttu-id="740d2-134">**IMAPIProp** および他のインターフェイスのメソッドの多くは、プロパティを記述するために **SPropTagArray** 構造体を使用します。</span><span class="sxs-lookup"><span data-stu-id="740d2-134">Many of the methods in **IMAPIProp** and other interfaces use an **SPropTagArray** structure for describing properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="740d2-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="740d2-135">See also</span></span>



[<span data-ttu-id="740d2-136">MAPI の概念</span><span class="sxs-lookup"><span data-stu-id="740d2-136">MAPI Concepts</span></span>](mapi-concepts.md)

