---
title: PidTagMemberName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberName
api_type:
- HeaderDef
ms.assetid: e19129bf-d07c-4d2e-9d4d-edbfda088ea7
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a119cf1446600153e433c4aae99037d9810015c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342484"
---
# <a name="pidtagmembername-canonical-property"></a>PidTagMemberName 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アクセス制御リスト (ACL) テーブルのメンバーの表示名を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_MEMBER_NAME、PR_MEMBER_NAME_A、PR_MEMBER_NAME_W  <br/> |
|識別子:  <br/> |0x6672  <br/> |
|データの種類 :   <br/> |PT_STRING8  <br/> |
|エリア:  <br/> |アクセス制御  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティは [、IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) インターフェイスで使用され、フォルダーまたはメールボックスに対する明示的な権限を持つユーザーまたはロールである ACL テーブルのメンバーの名前を表示します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> サーバーに保存されているフォルダーのアクセス許可リストの取得を処理します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

