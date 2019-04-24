---
title: PidTagLastModificationTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLastModificationTime
api_type:
- HeaderDef
ms.assetid: a64e5300-6865-4588-8e1b-158cfd9c60c2
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: dea709b457e28efef62718fc388621e01c4eb5bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279710"
---
# <a name="pidtaglastmodificationtime-canonical-property"></a>PidTagLastModificationTime 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オブジェクトまたはサブオブジェクトが最後に変更された日付と時刻を格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_LAST_MODIFICATION_TIME  <br/> |
|識別子:  <br/> |0x3008  <br/> |
|データの種類 :   <br/> |PT_SYSTIME  <br/> |
|エリア:  <br/> |メッセージ時間  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは、最初は**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md)) プロパティと同じ値に設定されます。 添付ファイルサブオブジェクトは、ネイティブファイルシステムによって管理される最終変更時刻をコピーすることによって、必要に応じて更新できます。 クライアントアプリケーションは、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを最初に呼び出すまで、このプロパティを設定できます。 プロバイダーでは、PR_LAST_MODIFICATION_TIME は、すべての**imapiprop:: SaveChanges**呼び出し中に、 **** を更新する必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルオブジェクトを処理します。
    
[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> サーバーとクライアントの間でメッセージオブジェクトデータの同期を処理します。
    
[[OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> ユーザー、連絡先、グループ、およびリソースのリストのプロパティと操作を指定します。
    
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

