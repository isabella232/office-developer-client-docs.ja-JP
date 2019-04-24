---
title: PidLidFlagRequest 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFlagRequest
api_type:
- COM
ms.assetid: 38981f07-14b8-47c2-93df-e6aed91896e4
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ddcf32df716fe2b0a02655278ff0cd8d821de1f4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357807"
---
# <a name="pidlidflagrequest-canonical-property"></a>PidLidFlagRequest 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
会議出席依頼の状態を表します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidrequest  <br/> |
|プロパティセット:  <br/> |PSETID_Common  <br/> |
|ロング ID (LID):  <br/> |0x00008530  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|エリア:  <br/> |フラグ  <br/> |
   
## <a name="remarks"></a>解説

Microsoft Office Outlook では、会議出席依頼は予定アイテムです。
  
このプロパティには、フラグに関連付けられる specifiable テキストが含まれていますが、メッセージオブジェクトがフラグ付きまたは完了済みであり、会議関連オブジェクトに対して存在してはならない場合に設定する必要があります。 このプロパティを設定する必要がある場合は、クライアントがこのプロパティをサポートしないようにして、常に "フォローアップ" (必要な場合は、ユーザーの言語に変換されます) を文字列の値として記述します。 このプロパティは、 **dispidflagstringenum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)) プロパティと**dispidvalidflagstringプルーフ**([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)) プロパティの値に基づいて、条件付きで無視される必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> フラグに関連するプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

