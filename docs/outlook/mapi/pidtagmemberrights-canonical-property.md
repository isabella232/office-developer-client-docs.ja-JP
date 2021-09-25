---
title: PidTagMemberRights 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagMemberRights
api_type:
- HeaderDef
ms.assetid: 3e526b93-1f64-41ea-b43c-5b03fe1c56ed
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b2adbd44107b07ac73e04bb7dbe2b3d87fae4bbf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595204"
---
# <a name="pidtagmemberrights-canonical-property"></a>PidTagMemberRights 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォルダーまたはメールボックスに対するこのメンバーの権限を示す一連のビットが含まれる。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_MEMBER_RIGHTS  <br/> |
|識別子:  <br/> |0x6673  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |アクセス制御  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは [、IExchangeModifyTable](iexchangemodifytableiunknown.md) インターフェイスで、フォルダー上のメンバーの権限を定義するために使用されます。 これらの権限は、表示および変更できます。 次の値は、このプロパティに対して定義されている権限です。 
  
frightsReadAny
  
> メンバーは、任意のメッセージを読み取りできます。
    
frightsCreate
  
> メンバーはメッセージを作成できます。
    
frightsEditOwned
  
> メンバーは、ユーザーが所有するメッセージを編集できます。
    
frightsDeleteOwned
  
> メンバーは、ユーザーが所有するメッセージを削除できます。
    
frightsEditAny
  
> メンバーは、任意のメッセージを編集できます。
    
frightsDeleteAny
  
> メンバーは、任意のメッセージを削除できます。
    
frightsCreateSubfolder
  
> メンバーは、フォルダーのサブフォルダーを作成できます。
    
frightsOwner
  
> メンバーは、フォルダーに対する以前のすべての権限を持っています。
    
frightsContact
  
> メンバーは、自分の名前をフォルダーの連絡先として表示できます。
    
frightsVisible
  
> メンバーは、フォルダーが存在することを確認できます。
    
rightsNone
  
> メンバーはフォルダーに対する権限を持つ必要があります。
    
rightsReadOnly
  
> メンバーは、フォルダー内の任意のメッセージを読み取ります。
    
rightsReadWrite
  
> メンバーは、フォルダー内の任意のメッセージの読み取りおよび書き込みを行います。
    
rightsAll
  
> メンバーは、フォルダーに対する以前のすべての権限を持っています。
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> フォルダー操作を処理します。
    
[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> サーバーに保存されているフォルダーのアクセス許可リストの取得を処理します。
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> メールボックスを代理人として接続および構成するためのメソッド、および他のユーザーに代わって動作するメッセージアイテムと予定表アイテムとのやり取りを指定します。
    
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

