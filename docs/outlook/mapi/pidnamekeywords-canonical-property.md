---
title: PidNameKeywords 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameKeywords
api_type:
- COM
ms.assetid: bcc0cda0-02bc-49a5-9fb9-850b4c2867c1
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 90e5b370dace12dbe529465259b8551516fda491
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386370"
---
# <a name="pidnamekeywords-canonical-property"></a>PidNameKeywords 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
キーワードやメッセージのオブジェクトのカテゴリが含まれています。
  
|||
|:-----|:-----|
|フレンドリ名:  <br/> |なし  <br/> |
|プロパティを設定します。  <br/> |PS_PUBLIC_STRINGS  <br/> |
|プロパティ名:  <br/> |Keywords  <br/> |
|データの種類 :   <br/> |PT_MV_UNICODE  <br/> |
|エリア:  <br/> |メッセージ全般  <br/> |
   
## <a name="remarks"></a>備考

メッセージのオブジェクトでは、このプロパティの複数値文字列内の各文字列の長さのカテゴリを指定する複数行文字列値は 256 未満である必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
[[MS OXODOC]](https://msdn.microsoft.com/library/103007c8-5066-4bed-84e3-4465907af098%28Office.15%29.aspx)
  
> プロパティは、ドキュメントに対する許可の操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

