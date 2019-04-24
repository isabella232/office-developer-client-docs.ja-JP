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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2d57e6a195036ead9eb42666876e91a72f65eb8b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331298"
---
# <a name="pidlidsideeffects-canonical-property"></a>PidLidSideEffects 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
エンドユーザーの入力に対してアクションを処理するときに、クライアントがメッセージオブジェクトを処理する方法を制御します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidsideeffects  <br/> |
|プロパティセット:  <br/> |PSETID_Common  <br/> |
|ロング ID (LID):  <br/> |0x00008510  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |実行時の構成  <br/> |
   
## <a name="remarks"></a>解説

次のフラグのビット単位または0以上に設定する必要があります。
  
|**名前**|**値**|**説明**|
|:-----|:-----|:-----|
|seOpenToDelete  <br/> |0x0001  <br/> |メッセージオブジェクトを削除するときに、追加の処理が必要になります。  <br/> |
|senoframe  <br/> |0x0008  <br/> |メッセージオブジェクトに関連付けられている UI はありません。  <br/> |
|secoercetoinbox  <br/> |0x0010  <br/> |"IPF" という**PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) プロパティを使用して folder オブジェクトに移動またはコピーするときは、message オブジェクトで追加の処理が必要になります。メモ "です。  <br/> |
|seOpenTocopy  <br/> |0x0020  <br/> |別のフォルダーにコピーする場合は、message オブジェクトで追加の処理が必要になります。  <br/> |
|seopentomove  <br/> |0x0040  <br/> |別のフォルダーに移動するときは、message オブジェクトで追加の処理が必要になります。  <br/> |
|seopenforctxmenu  <br/> |0x0100  <br/> |動詞をエンドユーザーに表示するときは、message オブジェクトで追加の処理が必要になります。  <br/> |
|seCannotUndoDelete  <br/> |0x0400  <br/> |削除操作を元に戻すことはできません。 "seOpenToDelete" が設定されていない限り、設定することはできません。  <br/> |
|seCannotUndoCopy  <br/> |0x0800  <br/> |コピー操作を元に戻すことはできません。 "seOpenTocopy" が設定されていない限り、設定することはできません。  <br/> |
|seCannotUndoMove  <br/> |0x1000  <br/> |移動操作を元に戻すことはできません。 "seopentomove" が設定されている場合を除き、設定しないでください。  <br/> |
|seHasScript  <br/> |0x2000  <br/> |メッセージオブジェクトには、エンドユーザースクリプトが含まれています。  <br/> |
|seOpenToPermDelete  <br/> |0x4000  <br/> |message オブジェクトを完全に削除するには、追加の処理が必要です。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルオブジェクトを処理します。
    
[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> 予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

