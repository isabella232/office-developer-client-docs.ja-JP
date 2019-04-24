---
title: PidTagRoamingBinary 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f06bf063-fc95-46f9-b5fa-3f127a59ebda
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ead7c9c33c92240ba5e458b68635b766caaa9760
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359564"
---
# <a name="pidtagroamingbinary-canonical-property"></a>PidTagRoamingBinary 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
IPM のサブクラスに関連付けられたメッセージストリームを含み**ます。構成**クラス。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ROAMING_BINARYSTREAM  <br/> |
|識別子:  <br/> |0x7C09  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |構成  <br/> |
   
## <a name="remarks"></a>解説

このプロパティには、IPM に関連付けられているデータストリームが含まれ**ます。構成**メッセージクラスメッセージ。 stream の形式は、メッセージクラスに依存します。 たとえば、クラスの種類が IPM であるメッセージ **。構成。オートコンプリート**は、[オートコンプリートストリーム](autocomplete-stream.md)として書式設定されます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Microsoft Exchange Server プロトコルの仕様への参照を提供します。
    
[[OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> カテゴリの共有リストや稼働時間など、クライアントおよびサーバーの構成データの場所とプロパティを指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 関連するプロパティとしてリストされているプロパティの定義が含まれます。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

