---
title: PidTagRtfSyncBodyCrc 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncBodyCrc
api_type:
- COM
ms.assetid: 95db4837-400f-476f-b313-60e8baa1c6d1
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 85ac61d968243283e5ad9283730941adcd87cd5e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357870"
---
# <a name="pidtagrtfsyncbodycrc-canonical-property"></a>PidTagRtfSyncBodyCrc 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージテキストに対して計算された巡回冗長検査 (CRC) を含みます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RTF_SYNC_BODY_CRC  <br/> |
|識別子:  <br/> |0x1006  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI メッセージ  <br/> |
   
## <a name="remarks"></a>解説

[rtfsync](rtfsync.md)関数は、メッセージに対して有意と見なされる文字のみを使用して CRC を計算します。 たとえば、一部の空白文字とその他の無視できる文字は、CRC で省略されています。 
  
このプロパティは、リッチテキスト形式 (RTF) の補助プロパティです。 これらのプロパティは、 **rtfsync**関数で使用され、クライアントアプリケーションによって直接使用されることを意図したものではありません。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> メッセージと添付ファイルオブジェクトをエンコードし、効率的なストリーム表現にデコードします。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

