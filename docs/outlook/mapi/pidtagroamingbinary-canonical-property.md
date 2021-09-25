---
title: PidTagRoamingBinary 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f06bf063-fc95-46f9-b5fa-3f127a59ebda
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3e948b4085e002832df9657d61c87962af9b9fdb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59555154"
---
# <a name="pidtagroamingbinary-canonical-property"></a>PidTagRoamingBinary 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
IPM のサブクラスに関連付けられたメッセージ ストリームが **含まれます。構成** クラス。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ROAMING_BINARYSTREAM  <br/> |
|識別子:  <br/> |0x7C09  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |構成  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティには、IPM に関連付けられたデータ ストリーム **が含まれます。構成** メッセージ クラス メッセージ。 ストリームの形式は、メッセージ クラスによって異なります。 たとえば、クラスの種類 **IPM のメッセージです。Configuration.Autocomplete** はオートコンプリート ストリームとして [書式設定されます](autocomplete-stream.md)。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのMicrosoft Exchange Server提供します。
    
[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> 共有カテゴリ リストや作業時間など、クライアントおよびサーバー構成データの場所とプロパティを指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

