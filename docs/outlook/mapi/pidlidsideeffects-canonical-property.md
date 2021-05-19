---
title: PidLidSideEffects 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSideEffects
api_type:
- COM
ms.assetid: 90d601d9-5eeb-40b6-885d-ccd8a95ae322
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2d57e6a195036ead9eb42666876e91a72f65eb8b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331298"
---
# <a name="pidlidsideeffects-canonical-property"></a>PidLidSideEffects 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
エンド ユーザー入力に対する処理時にクライアントがメッセージ オブジェクトを処理する方法を制御します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidSideEffects  <br/> |
|プロパティ セット:  <br/> |PSETID_Common  <br/> |
|長い ID (LID):  <br/> |0x00008510  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |実行時の構成  <br/> |
   
## <a name="remarks"></a>注釈

次のフラグのビットまたは 0 以上に設定する必要があります。
  
|**名前**|**値**|**説明**|
|:-----|:-----|:-----|
|seOpenToDelete  <br/> |0x0001  <br/> |削除する場合は、メッセージ オブジェクトに対して追加の処理が必要です。  <br/> |
|seNoFrame  <br/> |0x0008  <br/> |メッセージ オブジェクトに関連付けられた UI はありません。  <br/> |
|seCoerceToInbox  <br/> |0x0010  <br/> |"IPF" の **PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) プロパティを持つフォルダー オブジェクトに移動またはコピーする場合は、メッセージ オブジェクトに対して追加の処理が必要です。注」  <br/> |
|seOpenTocopy  <br/> |0x0020  <br/> |別のフォルダーにコピーする場合は、メッセージ オブジェクトに対して追加の処理が必要です。  <br/> |
|seOpenToMove  <br/> |0x0040  <br/> |別のフォルダーに移動する場合は、メッセージ オブジェクトに対して追加の処理が必要です。  <br/> |
|seOpenForCtxMenu  <br/> |0x0100  <br/> |エンドユーザーに動詞を表示する場合は、メッセージ オブジェクトに対して追加の処理が必要です。  <br/> |
|seCannotUndoDelete  <br/> |0x0400  <br/> |削除操作を元に戻すことはできません。"seOpenToDelete" が設定されていない場合は設定できません。  <br/> |
|seCannotUndoCopy  <br/> |0x0800  <br/> |コピー操作を元に戻すことはできません。"seOpenTocopy" が設定されていない場合は設定できません。  <br/> |
|seCannotUndoMove  <br/> |0x1000  <br/> |移動操作を元に戻すことはできません。"seOpenToMove" が設定されていない場合は設定できません。  <br/> |
|seHasScript  <br/> |0x2000  <br/> |message オブジェクトには、エンド ユーザー スクリプトが含まれる。  <br/> |
|seOpenToPermDelete  <br/> |0x4000  <br/> |メッセージ オブジェクトを完全に削除するには、追加の処理が必要です。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と、関連するプロトコル仕様Exchange Server提供します。
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージ オブジェクトと添付ファイル オブジェクトを処理します。
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> 予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

