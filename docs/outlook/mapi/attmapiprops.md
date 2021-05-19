---
title: attMAPIProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 806270c1-30e4-494e-9b03-7d1f2fc04099
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 185bfbb151c4f8d4e36b40b94393d14d50c33edf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410456"
---
# <a name="attmapiprops"></a><span data-ttu-id="2e0c2-103">attMAPIProps</span><span class="sxs-lookup"><span data-stu-id="2e0c2-103">attMAPIProps</span></span>

  
  
<span data-ttu-id="2e0c2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2e0c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2e0c2-105">**attMAPIProps** 属性は、既存の TNEF 定義属性のセットに対応していない MAPI プロパティをエンコードするために使用できる特別な属性です。</span><span class="sxs-lookup"><span data-stu-id="2e0c2-105">The **attMAPIProps** attribute is special in that it can be used to encode any MAPI property that does not have a counterpart in the set of existing TNEF-defined attributes.</span></span> <span data-ttu-id="2e0c2-106">属性データは、エンドツーエンドに配置された MAPI プロパティのカウントセットです。</span><span class="sxs-lookup"><span data-stu-id="2e0c2-106">The attribute data is a counted set of MAPI properties laid end-to-end.</span></span> <span data-ttu-id="2e0c2-107">MAPI プロパティの任意のセットを許可するこのエンコードの形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="2e0c2-107">The format of this encoding, which allows for any set of MAPI properties, is as follows:</span></span>  
  
 <span data-ttu-id="2e0c2-108">_Property_Seq:_</span><span class="sxs-lookup"><span data-stu-id="2e0c2-108">_Property_Seq:_</span></span>
  
> <span data-ttu-id="2e0c2-109">property-count  _Property_Value,..._</span><span class="sxs-lookup"><span data-stu-id="2e0c2-109">property-count  _Property_Value,..._</span></span>
    
<span data-ttu-id="2e0c2-110">プロパティカウント値が  _示Property_Value_ 数のアイテムが必要です。</span><span class="sxs-lookup"><span data-stu-id="2e0c2-110">There must be as many  _Property_Value_ items as the property-count value indicates.</span></span> 
  
 <span data-ttu-id="2e0c2-111">_Property_Value:_</span><span class="sxs-lookup"><span data-stu-id="2e0c2-111">_Property_Value:_</span></span>
  
> <span data-ttu-id="2e0c2-112">property-tag _Property_property-tag Proptag_Name  _プロパティ_</span><span class="sxs-lookup"><span data-stu-id="2e0c2-112">property-tag  _Property_property-tag  _Proptag_Name Property_</span></span>
    
<span data-ttu-id="2e0c2-113">プロパティ タグは、プロパティ識別子 [(PidTagSubject)](pidtagsubject-canonical-property.md)の0x0037001Fなど **PR_SUBJECT値** です。</span><span class="sxs-lookup"><span data-stu-id="2e0c2-113">The property-tag is simply the value associated with the property identifier, such as 0x0037001F for **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span></span>
  
 <span data-ttu-id="2e0c2-114">_プロパティ:_</span><span class="sxs-lookup"><span data-stu-id="2e0c2-114">_Property:_</span></span>
  
>  <span data-ttu-id="2e0c2-115">_Value_ value-count  _Value,..._</span><span class="sxs-lookup"><span data-stu-id="2e0c2-115">_Value_ value-count  _Value,..._</span></span>
    
 <span data-ttu-id="2e0c2-116">_Value:_</span><span class="sxs-lookup"><span data-stu-id="2e0c2-116">_Value:_</span></span>
  
> <span data-ttu-id="2e0c2-117">value-data value-size value-size value-data padding value-size value-IID value-data padding</span><span class="sxs-lookup"><span data-stu-id="2e0c2-117">value-data value-size value-data padding value-size value-IID value-data padding</span></span>
    
 <span data-ttu-id="2e0c2-118">_Proptag_Name:_</span><span class="sxs-lookup"><span data-stu-id="2e0c2-118">_Proptag_Name:_</span></span>
  
> <span data-ttu-id="2e0c2-119">name-guid name-kind name-id name-guid name-kind name-string-length name-string padding</span><span class="sxs-lookup"><span data-stu-id="2e0c2-119">name-guid name-kind name-id name-guid name-kind name-string-length name-string padding</span></span>
    
<span data-ttu-id="2e0c2-120">各プロパティのカプセル化は、プロパティ識別子とプロパティの種類によって異なります。</span><span class="sxs-lookup"><span data-stu-id="2e0c2-120">The encapsulation of each property varies based on the property identifier and the property type.</span></span> <span data-ttu-id="2e0c2-121">プロパティ タグ、識別子、および型は、Mapitags.h ヘッダー ファイルと Mapidefs.h ヘッダー ファイルで定義されます。</span><span class="sxs-lookup"><span data-stu-id="2e0c2-121">Property tags, identifiers, and types are defined in the Mapitags.h and Mapidefs.h header files.</span></span>
  
<span data-ttu-id="2e0c2-122">プロパティが名前付きプロパティの場合、プロパティ タグの直後に MAPI プロパティ名が続き、グローバル一意識別子 (GUID)、型、識別子または Unicode 文字列で構成されます。</span><span class="sxs-lookup"><span data-stu-id="2e0c2-122">If the property is a named property, then the property tag is immediately followed by the MAPI property name, consisting of a globally unique identifier (GUID), a type, and either an identifier or a Unicode string.</span></span>
  
<span data-ttu-id="2e0c2-123">PT_BINARY、PT_STRING8、PT_UNICODE、PT_OBJECT などの可変長の値を持つ複数値のプロパティとプロパティは、次のように扱います。</span><span class="sxs-lookup"><span data-stu-id="2e0c2-123">Multivalued properties and properties with variable length values, such as the PT_BINARY, PT_STRING8, PT_UNICODE, or PT_OBJECT property types, are treated in the following way.</span></span> <span data-ttu-id="2e0c2-124">最初に、32 ビット符号なし long としてエンコードされた値の数が TNEF ストリームに配置され、その後に個々の値が続きます。</span><span class="sxs-lookup"><span data-stu-id="2e0c2-124">First the number of values, encoded as a 32-bit unsigned long, is placed in the TNEF stream, followed by the individual values.</span></span> <span data-ttu-id="2e0c2-125">各プロパティの値データは、バイト単位のサイズとしてエンコードされ、その後に値データ自体が続きます。</span><span class="sxs-lookup"><span data-stu-id="2e0c2-125">Each property's value-data is encoded as its size in bytes followed by the value-data itself.</span></span> <span data-ttu-id="2e0c2-126">値データは 4 バイト境界に埋め込まれますが、埋め込み量は値サイズには含まれません。</span><span class="sxs-lookup"><span data-stu-id="2e0c2-126">The value-data is padded out to a 4-byte boundary, although the amount of padding is not included in the value-size.</span></span>
  
<span data-ttu-id="2e0c2-127">プロパティがオブジェクトの種類PT_OBJECT、値のサイズの後にオブジェクトのインターフェイス識別子が続きます。</span><span class="sxs-lookup"><span data-stu-id="2e0c2-127">If the property is of type PT_OBJECT, the value-size is followed by the interface identifier of the object.</span></span> <span data-ttu-id="2e0c2-128">TNEF の現在の実装では、インターフェイスIID_IMessage、IID_IStorage、IID_Istreamのみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="2e0c2-128">The current implementation of TNEF only supports the IID_IMessage, IID_IStorage, and IID_Istream interface identifiers.</span></span> <span data-ttu-id="2e0c2-129">インターフェイス識別子のサイズは、値サイズに含まれます。</span><span class="sxs-lookup"><span data-stu-id="2e0c2-129">The size of the interface identifier is included in the value-size.</span></span>
  
<span data-ttu-id="2e0c2-130">オブジェクトが埋め込みメッセージ (つまり、プロパティの種類が PT_OBJECT、インターフェイス識別子が IID_Imessage) の場合、値データは埋め込み TNEF ストリームとしてエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="2e0c2-130">If the object is an embedded message (that is, it has a property type of PT_OBJECT and an interface identifier of IID_Imessage), the value data is encoded as an embedded TNEF stream.</span></span> <span data-ttu-id="2e0c2-131">TNEF 実装での埋め込みメッセージの実際のエンコードは、元のストリームの 2 番目の TNEF オブジェクトを開き、ストリームをインラインで処理することで行われます。</span><span class="sxs-lookup"><span data-stu-id="2e0c2-131">The actual encoding of an embedded message in TNEF implementation is done by opening a second TNEF object for the original stream and processing the stream inline.</span></span>
  

