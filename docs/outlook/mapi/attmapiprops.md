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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318124"
---
# <a name="attmapiprops"></a><span data-ttu-id="df2e7-103">attMAPIProps</span><span class="sxs-lookup"><span data-stu-id="df2e7-103">attMAPIProps</span></span>

  
  
<span data-ttu-id="df2e7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df2e7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df2e7-105">**attMAPIProps**属性は特別で、既存の TNEF 定義属性のセットに対応するものがない MAPI プロパティをエンコードするために使用できます。</span><span class="sxs-lookup"><span data-stu-id="df2e7-105">The **attMAPIProps** attribute is special in that it can be used to encode any MAPI property that does not have a counterpart in the set of existing TNEF-defined attributes.</span></span> <span data-ttu-id="df2e7-106">属性データは、エンドツーエンドで配置された MAPI プロパティのカウントセットです。</span><span class="sxs-lookup"><span data-stu-id="df2e7-106">The attribute data is a counted set of MAPI properties laid end-to-end.</span></span> <span data-ttu-id="df2e7-107">このエンコードの形式は、どの MAPI プロパティでも使用できます。次のようになります。</span><span class="sxs-lookup"><span data-stu-id="df2e7-107">The format of this encoding, which allows for any set of MAPI properties, is as follows:</span></span>  
  
 <span data-ttu-id="df2e7-108">_Property_Seq:_</span><span class="sxs-lookup"><span data-stu-id="df2e7-108">_Property_Seq:_</span></span>
  
> <span data-ttu-id="df2e7-109">_Property_Value,..._ のプロパティ数</span><span class="sxs-lookup"><span data-stu-id="df2e7-109">property-count  _Property_Value,..._</span></span>
    
<span data-ttu-id="df2e7-110">プロパティ数の値が示すように、 _Property_Value_の項目数は多くなければなりません。</span><span class="sxs-lookup"><span data-stu-id="df2e7-110">There must be as many  _Property_Value_ items as the property-count value indicates.</span></span> 
  
 <span data-ttu-id="df2e7-111">_Property_Value:_</span><span class="sxs-lookup"><span data-stu-id="df2e7-111">_Property_Value:_</span></span>
  
> <span data-ttu-id="df2e7-112">プロパティ-tag _ プロパティ-tag _Proptag_Name プロパティ_</span><span class="sxs-lookup"><span data-stu-id="df2e7-112">property-tag  _Property_property-tag  _Proptag_Name Property_</span></span>
    
<span data-ttu-id="df2e7-113">プロパティのタグは、単にプロパティ識別子に関連付けられている値です。たとえば、 **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) の0x0037001f などです。</span><span class="sxs-lookup"><span data-stu-id="df2e7-113">The property-tag is simply the value associated with the property identifier, such as 0x0037001F for **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span></span>
  
 <span data-ttu-id="df2e7-114">_プロパティ_</span><span class="sxs-lookup"><span data-stu-id="df2e7-114">_Property:_</span></span>
  
>  <span data-ttu-id="df2e7-115">__ 値の値-count の値 _,..._</span><span class="sxs-lookup"><span data-stu-id="df2e7-115">_Value_ value-count  _Value,..._</span></span>
    
 <span data-ttu-id="df2e7-116">_Value:_</span><span class="sxs-lookup"><span data-stu-id="df2e7-116">_Value:_</span></span>
  
> <span data-ttu-id="df2e7-117">値-データの値-サイズ値-データパディング値-サイズ値-IID 値-データパディング</span><span class="sxs-lookup"><span data-stu-id="df2e7-117">value-data value-size value-data padding value-size value-IID value-data padding</span></span>
    
 <span data-ttu-id="df2e7-118">_Proptag_Name:_</span><span class="sxs-lookup"><span data-stu-id="df2e7-118">_Proptag_Name:_</span></span>
  
> <span data-ttu-id="df2e7-119">name-guid 名-種類 name-id name-guid name-kind name-string-length name-文字列のパディング</span><span class="sxs-lookup"><span data-stu-id="df2e7-119">name-guid name-kind name-id name-guid name-kind name-string-length name-string padding</span></span>
    
<span data-ttu-id="df2e7-120">各プロパティのカプセル化は、プロパティの識別子とプロパティの種類によって異なります。</span><span class="sxs-lookup"><span data-stu-id="df2e7-120">The encapsulation of each property varies based on the property identifier and the property type.</span></span> <span data-ttu-id="df2e7-121">プロパティタグ、識別子、および型は、Mapitags および mapidefs.h ヘッダーファイルで定義されています。</span><span class="sxs-lookup"><span data-stu-id="df2e7-121">Property tags, identifiers, and types are defined in the Mapitags.h and Mapidefs.h header files.</span></span>
  
<span data-ttu-id="df2e7-122">プロパティが名前付きプロパティの場合、プロパティタグの直後には、グローバル一意識別子 (GUID)、型、識別子または Unicode 文字列で構成される MAPI プロパティ名が付けられます。</span><span class="sxs-lookup"><span data-stu-id="df2e7-122">If the property is a named property, then the property tag is immediately followed by the MAPI property name, consisting of a globally unique identifier (GUID), a type, and either an identifier or a Unicode string.</span></span>
  
<span data-ttu-id="df2e7-123">PT_BINARY、PT_STRING8、PT_UNICODE、PT_OBJECT のプロパティの種類など、可変長の値を持つ複数値プロパティとプロパティは、次のように処理されます。</span><span class="sxs-lookup"><span data-stu-id="df2e7-123">Multivalued properties and properties with variable length values, such as the PT_BINARY, PT_STRING8, PT_UNICODE, or PT_OBJECT property types, are treated in the following way.</span></span> <span data-ttu-id="df2e7-124">最初に、32ビットの符号なし長としてエンコードされた値の数が TNEF ストリームに配置され、その後に個々の値が続きます。</span><span class="sxs-lookup"><span data-stu-id="df2e7-124">First the number of values, encoded as a 32-bit unsigned long, is placed in the TNEF stream, followed by the individual values.</span></span> <span data-ttu-id="df2e7-125">各プロパティの値は、バイト単位のサイズとして、値データそのものでエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="df2e7-125">Each property's value-data is encoded as its size in bytes followed by the value-data itself.</span></span> <span data-ttu-id="df2e7-126">値データは、4バイト境界に埋め込まれます。ただし、値のサイズには埋め込まれている量は含まれません。</span><span class="sxs-lookup"><span data-stu-id="df2e7-126">The value-data is padded out to a 4-byte boundary, although the amount of padding is not included in the value-size.</span></span>
  
<span data-ttu-id="df2e7-127">プロパティの型が PT_OBJECT の場合は、値の後にオブジェクトのインターフェイス識別子が続きます。</span><span class="sxs-lookup"><span data-stu-id="df2e7-127">If the property is of type PT_OBJECT, the value-size is followed by the interface identifier of the object.</span></span> <span data-ttu-id="df2e7-128">現在の TNEF の実装では、IID_IMessage、IID_IStorage、および IID_Istream のインターフェイス識別子のみがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="df2e7-128">The current implementation of TNEF only supports the IID_IMessage, IID_IStorage, and IID_Istream interface identifiers.</span></span> <span data-ttu-id="df2e7-129">インターフェイス識別子のサイズは、値のサイズに含まれています。</span><span class="sxs-lookup"><span data-stu-id="df2e7-129">The size of the interface identifier is included in the value-size.</span></span>
  
<span data-ttu-id="df2e7-130">オブジェクトが埋め込みメッセージの場合 (つまり、プロパティの種類が PT_OBJECT で、インターフェイス識別子が IID_Imessage の場合)、値データは埋め込み TNEF ストリームとしてエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="df2e7-130">If the object is an embedded message (that is, it has a property type of PT_OBJECT and an interface identifier of IID_Imessage), the value data is encoded as an embedded TNEF stream.</span></span> <span data-ttu-id="df2e7-131">TNEF を実装する埋め込みメッセージの実際のエンコーディングは、元のストリームの2番目の TNEF オブジェクトを開いて、ストリームをインラインで処理することによって実行されます。</span><span class="sxs-lookup"><span data-stu-id="df2e7-131">The actual encoding of an embedded message in TNEF implementation is done by opening a second TNEF object for the original stream and processing the stream inline.</span></span>
  

