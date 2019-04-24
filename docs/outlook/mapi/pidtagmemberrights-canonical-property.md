---
title: PidTagMemberRights 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberRights
api_type:
- HeaderDef
ms.assetid: 3e526b93-1f64-41ea-b43c-5b03fe1c56ed
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: dcbf8a323f5178a5a2e39d0963dd19415ab835bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342695"
---
# <a name="pidtagmemberrights-canonical-property"></a>PidTagMemberRights 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォルダーまたはメールボックスでこのメンバーの権限を示す一連のビットを含みます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_MEMBER_RIGHTS  <br/> |
|識別子:  <br/> |0x6673  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |アクセス制御  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは、 [IExchangeModifyTable](iexchangemodifytableiunknown.md)インターフェイスで、フォルダーのメンバーの権限を定義するために使用されます。 これらの権限は、表示および変更できます。 次の値は、このプロパティに対して定義されている権限です。 
  
frightsReadAny
  
> メンバーは任意のメッセージを読み取ることができます。
    
frightsCreate
  
> メンバーはメッセージを作成できます。
    
frightsEditOwned
  
> メンバーは、ユーザーが所有するすべてのメッセージを編集できます。
    
frightsDeleteOwned
  
> メンバーは、ユーザーが所有するすべてのメッセージを削除できます。
    
frightsEditAny
  
> メンバーは任意のメッセージを編集できます。
    
frightsDeleteAny
  
> メンバーは任意のメッセージを削除できます。
    
frightsCreateSubfolder
  
> メンバーは、フォルダーのサブフォルダーを作成できます。
    
frightsOwner
  
> メンバーは、フォルダーに対する以前のすべての権限を持っています。
    
frightsContact
  
> メンバーは、フォルダーの連絡先として自分の名前を表示することができます。
    
frightsVisible
  
> メンバーはフォルダーが存在することを確認できます。
    
rightsNone
  
> メンバーにフォルダーに対する権限がありません。
    
rightsReadOnly
  
> メンバーは、フォルダー内の任意のメッセージを読み取ることができます。
    
rightsReadWrite
  
> メンバーは、フォルダー内のメッセージの読み取りおよび書き込みを行うことができます。
    
rightsAll
  
> メンバーは、フォルダーに対する以前のすべての権限を持っています。
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> フォルダー操作を処理します。
    
[[OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> サーバーに格納されているフォルダーのアクセス許可リストの取得を処理します。
    
[[OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> 代理人としてメールボックスに接続して構成するためのメソッド、および別のユーザーの代理として動作するときのメッセージと予定表のアイテムの相互作用を指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 関連するプロパティとしてリストされているプロパティの定義が含まれます。
    
## <a name="see-also"></a>関連項目



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

