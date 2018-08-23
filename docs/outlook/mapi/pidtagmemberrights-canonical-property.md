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
ms.openlocfilehash: 2ffc6973d2670402ec8095120eea3db02f529d0a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802978"
---
# <a name="pidtagmemberrights-canonical-property"></a>PidTagMemberRights 標準プロパティ

  
  
**適用対象**: Outlook 
  
フォルダーまたはメールボックスには、このメンバーの権限を指定するビットのセットが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_MEMBER_RIGHTS  <br/> |
|識別子:  <br/> |0x6673  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|領域:  <br/> |アクセス制御  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、フォルダーのメンバーの権限を定義するのには、 [IExchangeModifyTable](iexchangemodifytableiunknown.md)インターフェイスが使用します。 これらの権限を表示および変更できます。 次の値は、このプロパティに対して定義される権限です。 
  
frightsReadAny
  
> メンバーは、すべてのメッセージを読み取ることができます。
    
frightsCreate
  
> メンバーは、メッセージを作成できます。
    
frightsEditOwned
  
> メンバーは、ユーザーが所有するすべてのメッセージを編集できます。
    
frightsDeleteOwned
  
> メンバーは、ユーザーが所有するすべてのメッセージを削除できます。
    
frightsEditAny
  
> メンバーは、任意のメッセージを編集できます。
    
frightsDeleteAny
  
> メンバーは、任意のメッセージを削除できます。
    
frightsCreateSubfolder
  
> メンバーは、フォルダーのサブフォルダーを作成できます。
    
frightsOwner
  
> メンバーは、フォルダーの以前のすべての権限を持ちます。
    
frightsContact
  
> メンバーは、フォルダーの連絡先として表示される自分の名前を持つことができます。
    
frightsVisible
  
> メンバーは、フォルダーが存在することを確認できます。
    
rightsNone
  
> メンバーには、フォルダーの権限がありません。
    
rightsReadOnly
  
> メンバーは、フォルダー内のメッセージを読み取ることができます。
    
rightsReadWrite
  
> メンバーから読み書きできるフォルダー内のメッセージにします。
    
rightsAll
  
> メンバーは、フォルダーの以前のすべての権限を持ちます。
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> フォルダーの操作を処理します。
    
[[MS OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> サーバーに格納されているフォルダーのアクセス許可の一覧の取得を処理します。
    
[[MS OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> 接続し、別のユーザーに代わって動作する場合は、デリゲート、およびメッセージと予定表のアイテムとの対話としてメールボックスを構成するためのメソッドを指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

