---
title: attMAPIProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 806270c1-30e4-494e-9b03-7d1f2fc04099
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: eef480e8b024565ab282fb242a36336cd17384a1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799706"
---
# <a name="attmapiprops"></a><span data-ttu-id="d0fa5-103">attMAPIProps</span><span class="sxs-lookup"><span data-stu-id="d0fa5-103">attMAPIProps</span></span>

  
  
<span data-ttu-id="d0fa5-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d0fa5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d0fa5-105">**AttMAPIProps**属性は、TNEF で定義されている既存の属性のセットでこれに相当するがない任意の MAPI プロパティをエンコードするために使用できるという点で特殊です。</span><span class="sxs-lookup"><span data-stu-id="d0fa5-105">The **attMAPIProps** attribute is special in that it can be used to encode any MAPI property that does not have a counterpart in the set of existing TNEF-defined attributes.</span></span> <span data-ttu-id="d0fa5-106">属性データは、エンド ・ ツー ・ エンドの配置の MAPI プロパティの計算済のセットです。</span><span class="sxs-lookup"><span data-stu-id="d0fa5-106">The attribute data is a counted set of MAPI properties laid end-to-end.</span></span> <span data-ttu-id="d0fa5-107">任意の MAPI プロパティ セットのため、このエンコーディングの形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="d0fa5-107">The format of this encoding, which allows for any set of MAPI properties, is as follows:</span></span>  
  
 <span data-ttu-id="d0fa5-108">_Property_Seq。_</span><span class="sxs-lookup"><span data-stu-id="d0fa5-108">_Property_Seq:_</span></span>
  
> <span data-ttu-id="d0fa5-109">プロパティ カウント_プロパティ _ 値、._</span><span class="sxs-lookup"><span data-stu-id="d0fa5-109">property-count  _Property_Value,..._</span></span>
    
<span data-ttu-id="d0fa5-110">プロパティ カウント値は、_プロパティ _ 値_項目の数を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d0fa5-110">There must be as many  _Property_Value_ items as the property-count value indicates.</span></span> 
  
 <span data-ttu-id="d0fa5-111">_プロパティ _ 値。_</span><span class="sxs-lookup"><span data-stu-id="d0fa5-111">_Property_Value:_</span></span>
  
> <span data-ttu-id="d0fa5-112">プロパティ タグ _Property_property タグ_Proptag_Name のプロパティ_</span><span class="sxs-lookup"><span data-stu-id="d0fa5-112">property-tag  _Property_property-tag  _Proptag_Name Property_</span></span>
    
<span data-ttu-id="d0fa5-113">プロパティ タグは、単に**あるの PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) の 0x0037001F などのプロパティの識別子に関連付けられている値です。</span><span class="sxs-lookup"><span data-stu-id="d0fa5-113">The property-tag is simply the value associated with the property identifier, such as 0x0037001F for **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span></span>
  
 <span data-ttu-id="d0fa5-114">_プロパティ:_</span><span class="sxs-lookup"><span data-stu-id="d0fa5-114">_Property:_</span></span>
  
>  <span data-ttu-id="d0fa5-115">_値_の値のカウント_値に設定する._</span><span class="sxs-lookup"><span data-stu-id="d0fa5-115">_Value_ value-count  _Value,..._</span></span>
    
 <span data-ttu-id="d0fa5-116">_値:_</span><span class="sxs-lookup"><span data-stu-id="d0fa5-116">_Value:_</span></span>
  
> <span data-ttu-id="d0fa5-117">値-値サイズ値にデータ値のサイズの値の IID 値データのパディングのスペース</span><span class="sxs-lookup"><span data-stu-id="d0fa5-117">value-data value-size value-data padding value-size value-IID value-data padding</span></span>
    
 <span data-ttu-id="d0fa5-118">_Proptag_Name。_</span><span class="sxs-lookup"><span data-stu-id="d0fa5-118">_Proptag_Name:_</span></span>
  
> <span data-ttu-id="d0fa5-119">名前 guid 名のような名前 id 名前の guid 名のような名前の文字列の長さ名文字列内のスペース</span><span class="sxs-lookup"><span data-stu-id="d0fa5-119">name-guid name-kind name-id name-guid name-kind name-string-length name-string padding</span></span>
    
<span data-ttu-id="d0fa5-120">各プロパティのカプセル化は、プロパティの識別子とプロパティの型によって異なります。</span><span class="sxs-lookup"><span data-stu-id="d0fa5-120">The encapsulation of each property varies based on the property identifier and the property type.</span></span> <span data-ttu-id="d0fa5-121">プロパティ タグ、識別子、および種類は、Mapitags.h と Mapidefs.h のヘッダー ファイルで定義されます。</span><span class="sxs-lookup"><span data-stu-id="d0fa5-121">Property tags, identifiers, and types are defined in the Mapitags.h and Mapidefs.h header files.</span></span>
  
<span data-ttu-id="d0fa5-122">プロパティが名前付きプロパティの場合は、し、プロパティ タグは、直後に MAPI プロパティ名が表示され、グローバル一意識別子 (GUID)、型、および識別子または Unicode 文字列で構成されます。</span><span class="sxs-lookup"><span data-stu-id="d0fa5-122">If the property is a named property, then the property tag is immediately followed by the MAPI property name, consisting of a globally unique identifier (GUID), a type, and either an identifier or a Unicode string.</span></span>
  
<span data-ttu-id="d0fa5-123">複数値を持つプロパティと PT_BINARY、PT_STRING8、PT_UNICODE、または PT_OBJECT プロパティの種類などの可変長の値を持つプロパティは、次のように扱われます。</span><span class="sxs-lookup"><span data-stu-id="d0fa5-123">Multivalued properties and properties with variable length values, such as the PT_BINARY, PT_STRING8, PT_UNICODE, or PT_OBJECT property types, are treated in the following way.</span></span> <span data-ttu-id="d0fa5-124">まず、符号なし 32 ビットとしてエンコードされた値の数は、個々 の値の後に、TNEF ストリームに置かれます。</span><span class="sxs-lookup"><span data-stu-id="d0fa5-124">First the number of values, encoded as a 32-bit unsigned long, is placed in the TNEF stream, followed by the individual values.</span></span> <span data-ttu-id="d0fa5-125">各プロパティの値のデータは、値のデータ自体に続くバイトのサイズとしてエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="d0fa5-125">Each property's value-data is encoded as its size in bytes followed by the value-data itself.</span></span> <span data-ttu-id="d0fa5-126">値のデータが水増しされます 4 バイト境界では、値のサイズのスペースの量が含まれていません。</span><span class="sxs-lookup"><span data-stu-id="d0fa5-126">The value-data is padded out to a 4-byte boundary, although the amount of padding is not included in the value-size.</span></span>
  
<span data-ttu-id="d0fa5-127">PT_OBJECT の種類のプロパティがある場合、オブジェクトのインターフェイス識別子値のサイズが続きます。</span><span class="sxs-lookup"><span data-stu-id="d0fa5-127">If the property is of type PT_OBJECT, the value-size is followed by the interface identifier of the object.</span></span> <span data-ttu-id="d0fa5-128">TNEF の現在の実装は、IID_IMessage、IID_IStorage、および IID_Istream のインタ フェース識別子をサポートするだけです。</span><span class="sxs-lookup"><span data-stu-id="d0fa5-128">The current implementation of TNEF only supports the IID_IMessage, IID_IStorage, and IID_Istream interface identifiers.</span></span> <span data-ttu-id="d0fa5-129">値のサイズでは、インターフェイス識別子のサイズが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d0fa5-129">The size of the interface identifier is included in the value-size.</span></span>
  
<span data-ttu-id="d0fa5-130">オブジェクトが埋め込みメッセージである場合 (これは、PT_OBJECT と IID_Imessage のインターフェイス識別子のプロパティの種類)、値のデータは、埋め込みの TNEF ストリームとしてエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="d0fa5-130">If the object is an embedded message (that is, it has a property type of PT_OBJECT and an interface identifier of IID_Imessage), the value data is encoded as an embedded TNEF stream.</span></span> <span data-ttu-id="d0fa5-131">TNEF の実装では埋め込みメッセージの実際のエンコーディングは、元のストリームの 2 つ目の TNEF オブジェクトを開くと、ストリームのインラインの処理によって行われます。</span><span class="sxs-lookup"><span data-stu-id="d0fa5-131">The actual encoding of an embedded message in TNEF implementation is done by opening a second TNEF object for the original stream and processing the stream inline.</span></span>
  

