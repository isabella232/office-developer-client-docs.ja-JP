---
title: PidTagStoreEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagStoreEntryId
api_type:
- COM
ms.assetid: 0d705667-19f4-4eda-a068-e65ea8f00d9b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e1e56668de79fedb37da8cbe47aca7c2e28e1d59
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550338"
---
# <a name="pidtagstoreentryid-canonical-property"></a>PidTagStoreEntryId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オブジェクトが存在するメッセージ ストアの一意のエントリ識別子を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_STORE_ENTRYID  <br/> |
|識別子:  <br/> |0x0FFB  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |ID プロパティ  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは [、IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) メソッドを使用してメッセージ ストアを開くのに使用されます。 また、メッセージ ストアが所有するオブジェクトを開く場合にも使用されます。 
  
メッセージ ストアの場合、このプロパティはストアの独自のプロパティ[(PidTagEntryId)](pidtagentryid-canonical-property.md)PR_ENTRYIDと同じです。 クライアント アプリケーションは [、IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) メソッドを使用して 2 つのプロパティを比較できます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージ オブジェクトと添付ファイル オブジェクトを処理します。
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> IETF RFC2445、RFC2446、RFC2447、および予定オブジェクトと会議オブジェクトの間で変換します。
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> フラグに関連するプロパティと操作を指定します。
    
[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> クライアント間でメールボックス フォルダーを共有します。
    
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

