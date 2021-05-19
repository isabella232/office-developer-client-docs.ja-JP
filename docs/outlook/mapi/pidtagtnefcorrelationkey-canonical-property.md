---
title: PidTagTnefCorrelationKey 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTnefCorrelationKey
api_type:
- COM
ms.assetid: a7f05c8c-59b4-4d5b-8e70-ebcde5f2ed45
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e38cf93523c14d2d58c48e24a79249674298b4b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341952"
---
# <a name="pidtagtnefcorrelationkey-canonical-property"></a>PidTagTnefCorrelationKey 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
トランスポート ニュートラル カプセル化形式 (TNEF) 添付ファイルとメッセージを関連付ける値を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_TNEF_CORRELATION_KEY  <br/> |
|識別子:  <br/> |0x007F  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |MAPI 封筒  <br/> |
   
## <a name="remarks"></a>注釈

TNEF 添付ファイルサブオブジェクトでこのプロパティを公開する必要があります。 このプロパティは、受信 TNEF ファイルが添付されているメッセージに属するかどうかを決定します。 これは、主にトランスポート プロバイダーとゲートウェイによって使用されます。
  
送信メッセージでは、トランスポート プロバイダーは、そのメッセージに固有のバイナリ値を計算するか、メッセージ識別子などの一意性要件を満たす既存の値を使用する必要があります。 トランスポート プロバイダーは、この値をこのプロパティに格納し [、ITnef::AddProps](itnef-addprops.md) メソッドを呼び出してカプセル化する必要があります。 メッセージ ヘッダーなど、プロバイダーによって定義された場所にも同じ値をトランスポート エンベロープに格納する必要があります。 
  
受信メッセージでは、トランスポート プロバイダーは [ITnef::ExtractProps](itnef-extractprops.md) メソッドを呼び出して TNEF 添付ファイルをカプセル化し、このプロパティをトランスポート エンベロープに格納されている値と比較する必要があります。 値が一致する場合は、TNEF を正常に処理する必要があります。つまり、TNEF 添付ファイルから抽出されたプロパティはすべて使用する必要があります。 値が一致しない場合は、TNEF 添付ファイルのすべてのプロパティを無視する必要があります。 このプロパティを設定しない場合、TNEF ファイルはこのメッセージに属すると見なされ、そこから抽出された他のプロパティを使用する必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> クライアントとサーバー間のデータ転送の順序とフローを処理します。
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> インターネット標準の電子メール規則からメッセージ オブジェクトに変換します。
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> メッセージオブジェクトと添付ファイル オブジェクトを効率的なストリーム表現にエンコードおよびデコードします。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

