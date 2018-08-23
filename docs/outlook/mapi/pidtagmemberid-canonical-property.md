---
title: PidTagMemberId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberId
api_type:
- HeaderDef
ms.assetid: 64faef3c-27b2-49d2-9d0c-8b9d33f1cb71
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ce6925f40e09261494e4edbcbd7314728debbe2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802985"
---
# <a name="pidtagmemberid-canonical-property"></a>PidTagMemberId 標準プロパティ

  
  
**適用対象**: Outlook 
  
権限を持つ、説明されている Microsoft Exchange Server のフォルダーまたはメールボックスのテーブルのメンバーの識別子が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_MEMBER_ID  <br/> |
|識別子:  <br/> |0x6671  <br/> |
|データの種類 :   <br/> |PT_I8  <br/> |
|領域:  <br/> |アクセス制御  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティでは、テーブルに一意な識別子を返します。 ディレクトリのユーザー id は、各メンバーの識別子に関連付けられたし、はこのプロパティで指定します。 このプロパティは、フォルダーに対する明示的な権限を持つメンバーのディレクトリ エントリの識別子を取得するために[IExchangeModifyTable](iexchangemodifytableiunknown.md)インターフェイスが使用します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> サーバーに格納されているフォルダーのアクセス許可の一覧の取得を処理します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagMemberEntryId 標準プロパティ](pidtagmemberentryid-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

