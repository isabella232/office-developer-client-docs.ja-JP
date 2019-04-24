---
title: PidTagOriginalSubject 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSubject
api_type:
- COM
ms.assetid: 8668ba4f-3236-4a87-a5aa-9cf7eea3d87b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: de957c33165cc96eec82bf95c8f292c5b323676a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331144"
---
# <a name="pidtagoriginalsubject-canonical-property"></a>PidTagOriginalSubject 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージに関するレポートで使用する、元のメッセージの件名を含みます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ORIGINAL_SUBJECT、PR_ORIGINAL_SUBJECT_A、PR_ORIGINAL_SUBJECT_W  <br/> |
|識別子:  <br/> |0x0049  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |一般的なメッセージング  <br/> |
   
## <a name="remarks"></a>解説

これらのプロパティは、最初は**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) プロパティと同じ値に設定されています。
  
件名のプロパティは通常、256文字未満の小さな文字列で、メッセージストアプロバイダーは、オブジェクトのリンクと埋め込み (OLE) **IStream**インターフェイスをサポートする義務を持ちません。 クライアントは、常に**imapiprop**インターフェイスを使用してアクセスを試行し、 **MAPI_E_NOT_ENOUGH_MEMORY**が返された場合にのみ**IStream**に頼る必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> サーバーとクライアントの間でメッセージオブジェクトデータの同期を処理します。
    
[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メールメッセージオブジェクトで許容されるプロパティと操作を指定します。
    
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

