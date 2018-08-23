---
title: MAPI Property Overview
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02e5b23f-1bdb-4fbf-a27d-e3301a359573
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 40a71592e658110dab81c9bcb4aec97f9930d014
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576478"
---
# <a name="mapi-property-overview"></a><span data-ttu-id="0183c-103">MAPI Property Overview</span><span class="sxs-lookup"><span data-stu-id="0183c-103">MAPI Property Overview</span></span>

  
  
<span data-ttu-id="0183c-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0183c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0183c-105">プロパティは、MAPI オブジェクトの属性です。</span><span class="sxs-lookup"><span data-stu-id="0183c-105">A property is an attribute of a MAPI object.</span></span> <span data-ttu-id="0183c-106">プロパティは、メッセージまたはメッセージのユーザーのアドレスの種類の [件名] 行などのオブジェクトについて何かを記述します。</span><span class="sxs-lookup"><span data-stu-id="0183c-106">Properties describe something about the object, such as the subject line of a message or the address type of a messaging user.</span></span> <span data-ttu-id="0183c-107">MAPI では、多くのオブジェクトを記述するいくつかおよびいくつかに該当する特定の種類のオブジェクトに対してのみ、多くのプロパティを定義します。</span><span class="sxs-lookup"><span data-stu-id="0183c-107">MAPI defines many properties, some to describe many objects and some that are appropriate only for an object of a particular type.</span></span> <span data-ttu-id="0183c-108">クライアントとサービス ・ プロバイダーは、新しいカスタム プロパティを作成することで MAPI の一連の定義済みのプロパティを拡張できます。</span><span class="sxs-lookup"><span data-stu-id="0183c-108">Clients and service providers can extend MAPI's set of predefined properties by creating new, custom properties.</span></span> <span data-ttu-id="0183c-109">クライアントは、新しいメッセージ クラスを記述するプロパティを定義でき、サービス プロバイダーは、ユーザーのメッセージング システムの独自の機能を公開するプロパティを定義できます。</span><span class="sxs-lookup"><span data-stu-id="0183c-109">Clients can define properties to describe new message classes, and service providers can define properties to expose the unique features of their messaging system.</span></span>
  
<span data-ttu-id="0183c-110">プロパティは、永続的または一時的にできます。</span><span class="sxs-lookup"><span data-stu-id="0183c-110">Properties can be persistent or temporary.</span></span> <span data-ttu-id="0183c-111">やプロファイルにそのオブジェクトのデータのセッションを永続化するプロパティを格納できます。</span><span class="sxs-lookup"><span data-stu-id="0183c-111">Properties that persist from session to session can be stored with their objects' data or in the profile.</span></span> <span data-ttu-id="0183c-112">一時プロパティは、現在のセッション中にのみ存在します。</span><span class="sxs-lookup"><span data-stu-id="0183c-112">Temporary properties exist only for the duration of the current session.</span></span> 
  
<span data-ttu-id="0183c-113">クライアントとサービス ・ プロバイダーは、テーブルまたはプロパティ シートのいずれかを持つユーザーにプロパティを表示できます。</span><span class="sxs-lookup"><span data-stu-id="0183c-113">Clients and service providers can show properties to users with either a table or a property sheet.</span></span> <span data-ttu-id="0183c-114">テーブルは、複数のオブジェクトに属するプロパティのいくつかの読み取り専用のビューを持つユーザーを提供します。</span><span class="sxs-lookup"><span data-stu-id="0183c-114">Tables provide users with a read-only view of some of the properties belonging to multiple objects.</span></span> <span data-ttu-id="0183c-115">オブジェクトとプロパティの各列を表すすべての行と行と列の形式でデータが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0183c-115">The data is displayed in row and column format, with each row representing an object and each column a property.</span></span> <span data-ttu-id="0183c-116">プロパティ シートは、1 つのオブジェクトに関連するプロパティが表示されるタブ付きダイアログ ボックスです。</span><span class="sxs-lookup"><span data-stu-id="0183c-116">Property sheets are tabbed dialog boxes that display related properties for a single object.</span></span> <span data-ttu-id="0183c-117">プロパティ シート読み取り専用か読み取り/書き込みアクセス権、データにします。</span><span class="sxs-lookup"><span data-stu-id="0183c-117">Property sheets can provide read-only or read/write access to the data.</span></span> <span data-ttu-id="0183c-118">プロパティ シートの実装者が変更を加えるユーザーを許可するかどうか。</span><span class="sxs-lookup"><span data-stu-id="0183c-118">Whether or not a user is allowed to make changes is up to the implementer of the property sheet.</span></span>
  
<span data-ttu-id="0183c-119">[IMAPIProp](imapipropiunknown.md)インターフェイスは、プロパティを操作するためのプライマリ インターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="0183c-119">The [IMAPIProp](imapipropiunknown.md) interface is the primary interface for working with properties.</span></span> <span data-ttu-id="0183c-120">**IMAPIProp**を実装するすべてのオブジェクトのプロパティをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="0183c-120">All objects that support properties implement **IMAPIProp**.</span></span> <span data-ttu-id="0183c-121">**IMAPIProp**には、プロパティ名とそれらの識別子との間のマッピングと、以前のエラーに関する情報を取得するプロパティの値を取得する、プロパティをコピー、変更を加えるし、それらの変更の保存メソッドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="0183c-121">**IMAPIProp** includes methods for retrieving property values, copying properties, making changes and saving those changes, mapping between property names and their identifiers, and retrieving information about a prior error.</span></span> 
  
<span data-ttu-id="0183c-122">プロパティおよびプロパティに関する情報を記述するためのいくつかのデータ構造体があります。</span><span class="sxs-lookup"><span data-stu-id="0183c-122">There are several data structures for describing properties and information about properties.</span></span> <span data-ttu-id="0183c-123">最も一般的に使用される構造体は、 [SPropValue](spropvalue.md)構造体および[SPropTagArray](sproptagarray.md)構造体です。</span><span class="sxs-lookup"><span data-stu-id="0183c-123">The most commonly used structures are the [SPropValue](spropvalue.md) structure and the [SPropTagArray](sproptagarray.md) structure.</span></span> <span data-ttu-id="0183c-124">**SPropValue**構造体には、プロパティを記述する 3 つ情報にはが含まれています。</span><span class="sxs-lookup"><span data-stu-id="0183c-124">The **SPropValue** structure contains the three pieces of information that describe a property:</span></span> 
  
- <span data-ttu-id="0183c-125">データ、またはプロパティの値です。</span><span class="sxs-lookup"><span data-stu-id="0183c-125">Data, or value, of the property.</span></span>
    
- <span data-ttu-id="0183c-126">整数またはブール値などのプロパティの値のデータ型です。</span><span class="sxs-lookup"><span data-stu-id="0183c-126">Data type of the property's value, such as integer or Boolean.</span></span> 
    
- <span data-ttu-id="0183c-127">プロパティおよび保守を担当するコンポーネントを一意に識別する特定の範囲内で数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="0183c-127">Numeric value within a particular range that uniquely identify the property and component responsible for maintaining it.</span></span> <span data-ttu-id="0183c-128">などのメッセージのメッセージ コンテンツのプロパティを保持するには、MAPI および別の範囲で定義されたプロパティは、カスタム メッセージ クラスを使用するクライアントによって定義されたコンテンツを保持する範囲があります。</span><span class="sxs-lookup"><span data-stu-id="0183c-128">For example, there is a range to hold message content properties defined by MAPI and another range to hold message content properties defined by a client for a custom message class.</span></span> 
    
<span data-ttu-id="0183c-129">プロパティの型と識別子は、プロパティ タグと呼ばれる 1 つのコンポーネントに結合されます。</span><span class="sxs-lookup"><span data-stu-id="0183c-129">The property type and identifier are combined into a single component called the property tag.</span></span> <span data-ttu-id="0183c-130">プロパティ タグは、プロパティを簡単に参照するために使用する定数です。</span><span class="sxs-lookup"><span data-stu-id="0183c-130">Property tags are constants that can be used to easily refer to the property.</span></span> <span data-ttu-id="0183c-131">MAPITAGS では、MAPI によって定義されているプロパティのプロパティ タグが含まれます。H ヘッダー ファイルと、 **ulPropTag** 、 **SPropValue**構造体のメンバーにします。</span><span class="sxs-lookup"><span data-stu-id="0183c-131">Property tags for properties defined by MAPI are included in the MAPITAGS.H header file and in the **ulPropTag** member of an **SPropValue** structure.</span></span> <span data-ttu-id="0183c-132">クライアントとサービス ・ プロバイダーは、識別、取得、および対応するプロパティを更新するプロパティ タグを使用します。</span><span class="sxs-lookup"><span data-stu-id="0183c-132">Clients and service providers use property tags to identify, retrieve, and update the corresponding properties.</span></span> 
  
<span data-ttu-id="0183c-133">**SPropTagArray**構造体は、プロパティ タグのカウント済み配列です。</span><span class="sxs-lookup"><span data-stu-id="0183c-133">The **SPropTagArray** structure is a counted array of property tags.</span></span> <span data-ttu-id="0183c-134">**IMAPIProp**およびその他のインターフェイスのメソッドの多くは、プロパティを記述する**SPropTagArray**構造体を使用します。</span><span class="sxs-lookup"><span data-stu-id="0183c-134">Many of the methods in **IMAPIProp** and other interfaces use an **SPropTagArray** structure for describing properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0183c-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="0183c-135">See also</span></span>



[<span data-ttu-id="0183c-136">MAPI の概念</span><span class="sxs-lookup"><span data-stu-id="0183c-136">MAPI Concepts</span></span>](mapi-concepts.md)

