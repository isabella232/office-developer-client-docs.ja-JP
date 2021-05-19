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
# <a name="attmapiprops"></a>attMAPIProps

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
**attMAPIProps** 属性は、既存の TNEF 定義属性のセットに対応していない MAPI プロパティをエンコードするために使用できる特別な属性です。 属性データは、エンドツーエンドに配置された MAPI プロパティのカウントセットです。 MAPI プロパティの任意のセットを許可するこのエンコードの形式は次のとおりです。  
  
 _Property_Seq:_
  
> property-count  _Property_Value,..._
    
プロパティカウント値が  _示Property_Value_ 数のアイテムが必要です。 
  
 _Property_Value:_
  
> property-tag _Property_property-tag Proptag_Name  _プロパティ_
    
プロパティ タグは、プロパティ識別子 [(PidTagSubject)](pidtagsubject-canonical-property.md)の0x0037001Fなど **PR_SUBJECT値** です。
  
 _プロパティ:_
  
>  _Value_ value-count  _Value,..._
    
 _Value:_
  
> value-data value-size value-size value-data padding value-size value-IID value-data padding
    
 _Proptag_Name:_
  
> name-guid name-kind name-id name-guid name-kind name-string-length name-string padding
    
各プロパティのカプセル化は、プロパティ識別子とプロパティの種類によって異なります。 プロパティ タグ、識別子、および型は、Mapitags.h ヘッダー ファイルと Mapidefs.h ヘッダー ファイルで定義されます。
  
プロパティが名前付きプロパティの場合、プロパティ タグの直後に MAPI プロパティ名が続き、グローバル一意識別子 (GUID)、型、識別子または Unicode 文字列で構成されます。
  
PT_BINARY、PT_STRING8、PT_UNICODE、PT_OBJECT などの可変長の値を持つ複数値のプロパティとプロパティは、次のように扱います。 最初に、32 ビット符号なし long としてエンコードされた値の数が TNEF ストリームに配置され、その後に個々の値が続きます。 各プロパティの値データは、バイト単位のサイズとしてエンコードされ、その後に値データ自体が続きます。 値データは 4 バイト境界に埋め込まれますが、埋め込み量は値サイズには含まれません。
  
プロパティがオブジェクトの種類PT_OBJECT、値のサイズの後にオブジェクトのインターフェイス識別子が続きます。 TNEF の現在の実装では、インターフェイスIID_IMessage、IID_IStorage、IID_Istreamのみをサポートしています。 インターフェイス識別子のサイズは、値サイズに含まれます。
  
オブジェクトが埋め込みメッセージ (つまり、プロパティの種類が PT_OBJECT、インターフェイス識別子が IID_Imessage) の場合、値データは埋め込み TNEF ストリームとしてエンコードされます。 TNEF 実装での埋め込みメッセージの実際のエンコードは、元のストリームの 2 番目の TNEF オブジェクトを開き、ストリームをインラインで処理することで行われます。
  

