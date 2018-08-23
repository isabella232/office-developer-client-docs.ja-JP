---
title: PidTagStoreEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreEntryId
api_type:
- COM
ms.assetid: 0d705667-19f4-4eda-a068-e65ea8f00d9b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 075c5e894d4b039ce06ca0508b838a7094af8768
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803583"
---
# <a name="pidtagstoreentryid-canonical-property"></a>PidTagStoreEntryId 標準プロパティ

  
  
**適用対象**: Outlook 
  
オブジェクトが格納されているメッセージ ストアの一意のエントリ id が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_STORE_ENTRYID  <br/> |
|識別子:  <br/> |0x0FFB  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|領域:  <br/> |ID プロパティ  <br/> |
   
## <a name="remarks"></a>注釈

[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)メソッドを使用してメッセージ ストアを開くには、このプロパティが使用されます。 メッセージ ・ ストアを所有している任意のオブジェクトを開くにも使用されます。 
  
メッセージ ・ ストアのこのプロパティは、ストアの**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) のプロパティと同じです。 クライアント アプリケーションは、 [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md)メソッドを使用して 2 つのプロパティを比較できます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。
    
[[MS OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> プロパティ フラグに関連する操作を指定します。
    
[[MS OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> クライアント間でのメールボックスのフォルダーを共有します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

