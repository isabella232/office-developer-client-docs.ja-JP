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
# <a name="attmapiprops"></a>attMAPIProps

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
**attMAPIProps**属性は特別で、既存の TNEF 定義属性のセットに対応するものがない MAPI プロパティをエンコードするために使用できます。 属性データは、エンドツーエンドで配置された MAPI プロパティのカウントセットです。 このエンコードの形式は、どの MAPI プロパティでも使用できます。次のようになります。  
  
 _Property_Seq:_
  
> _Property_Value,..._ のプロパティ数
    
プロパティ数の値が示すように、 _Property_Value_の項目数は多くなければなりません。 
  
 _Property_Value:_
  
> プロパティ-tag _ プロパティ-tag _Proptag_Name プロパティ_
    
プロパティのタグは、単にプロパティ識別子に関連付けられている値です。たとえば、 **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) の0x0037001f などです。
  
 _プロパティ_
  
>  __ 値の値-count の値 _,..._
    
 _Value:_
  
> 値-データの値-サイズ値-データパディング値-サイズ値-IID 値-データパディング
    
 _Proptag_Name:_
  
> name-guid 名-種類 name-id name-guid name-kind name-string-length name-文字列のパディング
    
各プロパティのカプセル化は、プロパティの識別子とプロパティの種類によって異なります。 プロパティタグ、識別子、および型は、Mapitags および mapidefs.h ヘッダーファイルで定義されています。
  
プロパティが名前付きプロパティの場合、プロパティタグの直後には、グローバル一意識別子 (GUID)、型、識別子または Unicode 文字列で構成される MAPI プロパティ名が付けられます。
  
PT_BINARY、PT_STRING8、PT_UNICODE、PT_OBJECT のプロパティの種類など、可変長の値を持つ複数値プロパティとプロパティは、次のように処理されます。 最初に、32ビットの符号なし長としてエンコードされた値の数が TNEF ストリームに配置され、その後に個々の値が続きます。 各プロパティの値は、バイト単位のサイズとして、値データそのものでエンコードされます。 値データは、4バイト境界に埋め込まれます。ただし、値のサイズには埋め込まれている量は含まれません。
  
プロパティの型が PT_OBJECT の場合は、値の後にオブジェクトのインターフェイス識別子が続きます。 現在の TNEF の実装では、IID_IMessage、IID_IStorage、および IID_Istream のインターフェイス識別子のみがサポートされています。 インターフェイス識別子のサイズは、値のサイズに含まれています。
  
オブジェクトが埋め込みメッセージの場合 (つまり、プロパティの種類が PT_OBJECT で、インターフェイス識別子が IID_Imessage の場合)、値データは埋め込み TNEF ストリームとしてエンコードされます。 TNEF を実装する埋め込みメッセージの実際のエンコーディングは、元のストリームの2番目の TNEF オブジェクトを開いて、ストリームをインラインで処理することによって実行されます。
  

