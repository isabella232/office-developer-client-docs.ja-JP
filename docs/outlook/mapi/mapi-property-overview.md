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
# <a name="mapi-property-overview"></a><span data-ttu-id="db926-103">MAPI のプロパティの概要</span><span class="sxs-lookup"><span data-stu-id="db926-103">MAPI Property Overview</span></span>

  
  
<span data-ttu-id="db926-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="db926-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="db926-105">プロパティは、MAPI オブジェクトの属性です。</span><span class="sxs-lookup"><span data-stu-id="db926-105">A property is an attribute of a MAPI object.</span></span> <span data-ttu-id="db926-106">プロパティは、メッセージの件名、メッセージングユーザーのアドレスの種類など、オブジェクトについての内容を示します。</span><span class="sxs-lookup"><span data-stu-id="db926-106">Properties describe something about the object, such as the subject line of a message or the address type of a messaging user.</span></span> <span data-ttu-id="db926-107">MAPI では、多くのプロパティを定義しています。複数のオブジェクトを記述する場合や、特定の種類のオブジェクトにのみ適している場合もあります。</span><span class="sxs-lookup"><span data-stu-id="db926-107">MAPI defines many properties, some to describe many objects and some that are appropriate only for an object of a particular type.</span></span> <span data-ttu-id="db926-108">クライアントおよびサービスプロバイダーは、新しいカスタムプロパティを作成することによって、あらかじめ定義されている MAPI のプロパティセットを拡張できます。</span><span class="sxs-lookup"><span data-stu-id="db926-108">Clients and service providers can extend MAPI's set of predefined properties by creating new, custom properties.</span></span> <span data-ttu-id="db926-109">クライアントは、新しいメッセージクラスを記述するためのプロパティを定義できます。また、サービスプロバイダーは、メッセージングシステムの固有の機能を公開するためのプロパティを定義できます。</span><span class="sxs-lookup"><span data-stu-id="db926-109">Clients can define properties to describe new message classes, and service providers can define properties to expose the unique features of their messaging system.</span></span>
  
<span data-ttu-id="db926-110">プロパティには、永続的なものと一時的なものがあります。</span><span class="sxs-lookup"><span data-stu-id="db926-110">Properties can be persistent or temporary.</span></span> <span data-ttu-id="db926-111">セッション間で保持されるプロパティは、オブジェクトのデータまたはプロファイルに格納できます。</span><span class="sxs-lookup"><span data-stu-id="db926-111">Properties that persist from session to session can be stored with their objects' data or in the profile.</span></span> <span data-ttu-id="db926-112">一時プロパティは、現在のセッションの期間だけ存在します。</span><span class="sxs-lookup"><span data-stu-id="db926-112">Temporary properties exist only for the duration of the current session.</span></span> 
  
<span data-ttu-id="db926-113">クライアントおよびサービスプロバイダーは、テーブルまたはプロパティシートを使用して、ユーザーにプロパティを表示できます。</span><span class="sxs-lookup"><span data-stu-id="db926-113">Clients and service providers can show properties to users with either a table or a property sheet.</span></span> <span data-ttu-id="db926-114">テーブルは、複数のオブジェクトに属するいくつかのプロパティの読み取り専用ビューをユーザーに提供します。</span><span class="sxs-lookup"><span data-stu-id="db926-114">Tables provide users with a read-only view of some of the properties belonging to multiple objects.</span></span> <span data-ttu-id="db926-115">データは行と列の形式で表示され、各行はオブジェクトを表し、各列がプロパティになります。</span><span class="sxs-lookup"><span data-stu-id="db926-115">The data is displayed in row and column format, with each row representing an object and each column a property.</span></span> <span data-ttu-id="db926-116">プロパティシートは、1つのオブジェクトの関連するプロパティを表示するタブ付きダイアログボックスです。</span><span class="sxs-lookup"><span data-stu-id="db926-116">Property sheets are tabbed dialog boxes that display related properties for a single object.</span></span> <span data-ttu-id="db926-117">プロパティシートは、読み取り専用または読み取り/書き込みのデータアクセスを提供できます。</span><span class="sxs-lookup"><span data-stu-id="db926-117">Property sheets can provide read-only or read/write access to the data.</span></span> <span data-ttu-id="db926-118">ユーザーがプロパティシートの実装者に変更を許可するかどうか。</span><span class="sxs-lookup"><span data-stu-id="db926-118">Whether or not a user is allowed to make changes is up to the implementer of the property sheet.</span></span>
  
<span data-ttu-id="db926-119">[imapiprop](imapipropiunknown.md)インターフェイスは、プロパティを使用するための主要なインターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="db926-119">The [IMAPIProp](imapipropiunknown.md) interface is the primary interface for working with properties.</span></span> <span data-ttu-id="db926-120">プロパティをサポートするすべてのオブジェクトは、 **imapiprop**を実装します。</span><span class="sxs-lookup"><span data-stu-id="db926-120">All objects that support properties implement **IMAPIProp**.</span></span> <span data-ttu-id="db926-121">**imapiprop**には、プロパティ値の取得、プロパティのコピー、変更、およびそれらの変更の保存、プロパティ名と識別子の間のマッピング、前のエラーに関する情報の取得を行うメソッドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="db926-121">**IMAPIProp** includes methods for retrieving property values, copying properties, making changes and saving those changes, mapping between property names and their identifiers, and retrieving information about a prior error.</span></span> 
  
<span data-ttu-id="db926-122">プロパティとプロパティに関する情報を記述するためのデータ構造がいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="db926-122">There are several data structures for describing properties and information about properties.</span></span> <span data-ttu-id="db926-123">最も一般的に使用される構造体は、 [spropvalue](spropvalue.md)構造体と[SPropTagArray](sproptagarray.md)構造体です。</span><span class="sxs-lookup"><span data-stu-id="db926-123">The most commonly used structures are the [SPropValue](spropvalue.md) structure and the [SPropTagArray](sproptagarray.md) structure.</span></span> <span data-ttu-id="db926-124">**spropvalue**構造体には、プロパティを説明する3つの情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="db926-124">The **SPropValue** structure contains the three pieces of information that describe a property:</span></span> 
  
- <span data-ttu-id="db926-125">プロパティのデータまたは値。</span><span class="sxs-lookup"><span data-stu-id="db926-125">Data, or value, of the property.</span></span>
    
- <span data-ttu-id="db926-126">プロパティの値のデータ型 (integer、Boolean など)。</span><span class="sxs-lookup"><span data-stu-id="db926-126">Data type of the property's value, such as integer or Boolean.</span></span> 
    
- <span data-ttu-id="db926-127">特定の範囲内で、そのプロパティとコンポーネントを保持する役割を一意に識別する数値。</span><span class="sxs-lookup"><span data-stu-id="db926-127">Numeric value within a particular range that uniquely identify the property and component responsible for maintaining it.</span></span> <span data-ttu-id="db926-128">たとえば、MAPI で定義されたメッセージコンテンツのプロパティを保持し、カスタムメッセージクラスに対してクライアントによって定義されたメッセージコンテンツのプロパティを保持する範囲があります。</span><span class="sxs-lookup"><span data-stu-id="db926-128">For example, there is a range to hold message content properties defined by MAPI and another range to hold message content properties defined by a client for a custom message class.</span></span> 
    
<span data-ttu-id="db926-129">プロパティの型と識別子は、プロパティタグと呼ばれる1つのコンポーネントに結合されます。</span><span class="sxs-lookup"><span data-stu-id="db926-129">The property type and identifier are combined into a single component called the property tag.</span></span> <span data-ttu-id="db926-130">プロパティタグは、プロパティを簡単に参照するために使用できる定数です。</span><span class="sxs-lookup"><span data-stu-id="db926-130">Property tags are constants that can be used to easily refer to the property.</span></span> <span data-ttu-id="db926-131">MAPI で定義されているプロパティのプロパティタグは、MAPITAGS に含まれています。H ヘッダーファイルと、 **spropvalue**構造の**ulPropTag**メンバ。</span><span class="sxs-lookup"><span data-stu-id="db926-131">Property tags for properties defined by MAPI are included in the MAPITAGS.H header file and in the **ulPropTag** member of an **SPropValue** structure.</span></span> <span data-ttu-id="db926-132">クライアントおよびサービスプロバイダーは、プロパティタグを使用して、対応するプロパティを識別、取得、更新します。</span><span class="sxs-lookup"><span data-stu-id="db926-132">Clients and service providers use property tags to identify, retrieve, and update the corresponding properties.</span></span> 
  
<span data-ttu-id="db926-133">**SPropTagArray**構造体は、プロパティタグのカウントされた配列です。</span><span class="sxs-lookup"><span data-stu-id="db926-133">The **SPropTagArray** structure is a counted array of property tags.</span></span> <span data-ttu-id="db926-134">**imapiprop**およびその他のインターフェイスのメソッドの多くは、プロパティを記述するために**SPropTagArray**構造を使用します。</span><span class="sxs-lookup"><span data-stu-id="db926-134">Many of the methods in **IMAPIProp** and other interfaces use an **SPropTagArray** structure for describing properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="db926-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="db926-135">See also</span></span>



[<span data-ttu-id="db926-136">MAPI の概念</span><span class="sxs-lookup"><span data-stu-id="db926-136">MAPI Concepts</span></span>](mapi-concepts.md)

