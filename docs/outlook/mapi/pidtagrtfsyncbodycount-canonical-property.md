---
title: PidTagRtfSyncBodyCount 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncBodyCount
api_type:
- COM
ms.assetid: b7267be4-8d5c-4dc7-86b2-651e03e84f9b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6f6e687412dfce1e5fcee6b4a4d64f3e5106455f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331256"
---
# <a name="pidtagrtfsyncbodycount-canonical-property"></a>PidTagRtfSyncBodyCount 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージテキストの重要な文字のカウントを含みます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RTF_SYNC_BODY_COUNT  <br/> |
|識別子:  <br/> |0x1007  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI メッセージ  <br/> |
   
## <a name="remarks"></a>解説

[rtfsync](rtfsync.md)関数は、メッセージに対して重要であると見なされているものだけを使用して、テキスト内の文字数を計算します。 たとえば、空白文字とその他の無視できる文字は、カウントから省略されています。 
  
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

