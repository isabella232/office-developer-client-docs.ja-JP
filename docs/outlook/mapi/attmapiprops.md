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
ms.openlocfilehash: 72f252791e374ed4b9b2a40c9b151ef2b91fefe6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588056"
---
# <a name="attmapiprops"></a>attMAPIProps

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
**AttMAPIProps**属性は、TNEF で定義されている既存の属性のセットでこれに相当するがない任意の MAPI プロパティをエンコードするために使用できるという点で特殊です。 属性データは、エンド ・ ツー ・ エンドの配置の MAPI プロパティの計算済のセットです。 任意の MAPI プロパティ セットのため、このエンコーディングの形式は次のとおりです。  
  
 _Property_Seq。_
  
> プロパティ カウント_プロパティ _ 値、._
    
プロパティ カウント値は、_プロパティ _ 値_項目の数を設定する必要があります。 
  
 _プロパティ _ 値。_
  
> プロパティ タグ _Property_property タグ_Proptag_Name のプロパティ_
    
プロパティ タグは、単に**あるの PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) の 0x0037001F などのプロパティの識別子に関連付けられている値です。
  
 _プロパティ:_
  
>  _値_の値のカウント_値に設定する._
    
 _値:_
  
> 値-値サイズ値にデータ値のサイズの値の IID 値データのパディングのスペース
    
 _Proptag_Name。_
  
> 名前 guid 名のような名前 id 名前の guid 名のような名前の文字列の長さ名文字列内のスペース
    
各プロパティのカプセル化は、プロパティの識別子とプロパティの型によって異なります。 プロパティ タグ、識別子、および種類は、Mapitags.h と Mapidefs.h のヘッダー ファイルで定義されます。
  
プロパティが名前付きプロパティの場合は、し、プロパティ タグは、直後に MAPI プロパティ名が表示され、グローバル一意識別子 (GUID)、型、および識別子または Unicode 文字列で構成されます。
  
複数値を持つプロパティと PT_BINARY、PT_STRING8、PT_UNICODE、または PT_OBJECT プロパティの種類などの可変長の値を持つプロパティは、次のように扱われます。 まず、符号なし 32 ビットとしてエンコードされた値の数は、個々 の値の後に、TNEF ストリームに置かれます。 各プロパティの値のデータは、値のデータ自体に続くバイトのサイズとしてエンコードされます。 値のデータが水増しされます 4 バイト境界では、値のサイズのスペースの量が含まれていません。
  
PT_OBJECT の種類のプロパティがある場合、オブジェクトのインターフェイス識別子値のサイズが続きます。 TNEF の現在の実装は、IID_IMessage、IID_IStorage、および IID_Istream のインタ フェース識別子をサポートするだけです。 値のサイズでは、インターフェイス識別子のサイズが含まれます。
  
オブジェクトが埋め込みメッセージである場合 (これは、PT_OBJECT と IID_Imessage のインターフェイス識別子のプロパティの種類)、値のデータは、埋め込みの TNEF ストリームとしてエンコードされます。 TNEF の実装では埋め込みメッセージの実際のエンコーディングは、元のストリームの 2 つ目の TNEF オブジェクトを開くと、ストリームのインラインの処理によって行われます。
  

