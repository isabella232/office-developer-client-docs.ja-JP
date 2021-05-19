---
title: PidTagCreationTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCreationTime
api_type:
- HeaderDef
ms.assetid: 13122af2-06c8-4342-983d-e38178743d8f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: de853c66f0ef4270f4c443881bfa163d4abfa3e0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357898"
---
# <a name="pidtagcreationtime-canonical-property"></a>PidTagCreationTime 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの作成日時を格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CREATION_TIME  <br/> |
|識別子:  <br/> |0x3007  <br/> |
|データの種類 :   <br/> |PT_SYSTIME  <br/> |
|エリア:  <br/> |メッセージ時刻  <br/> |
   
## <a name="remarks"></a>注釈

メッセージ ストアは、作成するメッセージごとにこのプロパティを設定します。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージ オブジェクトと添付ファイル オブジェクトを処理します。
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> ユーザー、連絡先、グループ、およびリソースの一覧のプロパティと操作を指定します。
    
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

