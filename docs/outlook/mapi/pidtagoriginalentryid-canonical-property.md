---
title: PidTagOriginalEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalEntryId
api_type:
- COM
ms.assetid: 8197d2c7-8665-41b8-bd3a-e9c1c2e642e9
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f3f4f42d91c4091943d6183508e2bc76c17197fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342722"
---
# <a name="pidtagoriginalentryid-canonical-property"></a>PidTagOriginalEntryId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アドレス帳から個人用アドレス帳または他の書き込み可能なアドレス帳にコピーされたエントリの元のエントリ識別子が含まれる。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ORIGINAL_ENTRYID  <br/> |
|識別子:  <br/> |0x3A12  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |一般的なメッセージング  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、コピーされたエントリの元のソースに関する情報を含むプロパティの 1 つです。
  
非読み取りレポートの場合、このプロパティには、レポートが生成された元のメッセージ受信者のエントリ識別子のコピーが含まれる。 元の受信者が配布リストの一部である場合、配布リストのエントリ識別子はレポートに対して保持されます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> ユーザー、連絡先、グループ、およびリソースの一覧のプロパティと操作を指定します。
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> サーバーとクライアント間のメッセージング オブジェクト データの同期を処理します。
    
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

