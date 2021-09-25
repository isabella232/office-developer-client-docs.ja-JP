---
title: PidLidFlagRequest 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidFlagRequest
api_type:
- COM
ms.assetid: 38981f07-14b8-47c2-93df-e6aed91896e4
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 536ec8f3922aadcf71eb89f67d4237efc0dfea5b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59555770"
---
# <a name="pidlidflagrequest-canonical-property"></a>PidLidFlagRequest 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
会議出席依頼の状態を表します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidRequest  <br/> |
|プロパティ セット:  <br/> |PSETID_Common  <br/> |
|長い ID (LID):  <br/> |0x00008530  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|エリア:  <br/> |フラグを設定する  <br/> |
   
## <a name="remarks"></a>注釈

このMicrosoft Office Outlook、会議出席依頼は予定アイテムです。
  
このプロパティには、フラグに関連付けられるユーザー指定可能なテキストが含まれているので、メッセージ オブジェクトにフラグが設定されている場合や完了した場合に設定する必要がありますが、会議関連オブジェクトには存在しません。 クライアントは、このプロパティをサポートしない選択をし、このプロパティを設定する必要がある場合は、常に "Follow up" (必要に応じてユーザーの言語に翻訳) を文字列の値として記述できます。 このプロパティは **、dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)) プロパティと **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)) プロパティの値に基づいて条件付きで無視する必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> フラグに関連するプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

