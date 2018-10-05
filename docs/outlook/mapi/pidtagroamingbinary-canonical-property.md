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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401672"
---
# <a name="pidtagroamingbinary-canonical-property"></a>PidTagRoamingBinary 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
**IPM のサブクラスに関連付けられているメッセージ ストリームが含まれています。構成**クラス。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ROAMING_BINARYSTREAM  <br/> |
|識別子:  <br/> |0x7C09  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |Configuration  <br/> |
   
## <a name="remarks"></a>備考

このプロパティには、IPM、**に関連付けられているデータ ストリームが含まれています。構成**メッセージ クラスのメッセージです。 ストリームの形式は、メッセージ クラスによって異なります。 たとえば、クラス型 IPM の**のメッセージです。Configuration.Autocomplete**ように、[オートコンプリートのストリーム](autocomplete-stream.md)としてフォーマットされます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Microsoft Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> 場所と共有カテゴリのリストおよび作業時間など、クライアントとサーバーの構成データのプロパティを指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

