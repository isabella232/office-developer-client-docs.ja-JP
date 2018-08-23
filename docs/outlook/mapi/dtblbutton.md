---
title: DTBLBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLBUTTON
api_type:
- COM
ms.assetid: 6058c78b-05d4-45a3-988c-1fbf8322125e
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e0797364eb4ec24793f64bad2f4d838507c236e4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571067"
---
# <a name="dtblbutton"></a>DTBLBUTTON

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
ディスプレイ テーブルから作成されたダイアログ ボックスのボタン コントロールに関する情報が含まれています。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連するマクロ:  <br/> |[SizedDtblButton](sizeddtblbutton.md) <br/> |
   
```cpp
typedef struct _DTBLBUTTON
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRControl;
} DTBLBUTTON, FAR *LPDTBLBUTTON;

```

## <a name="members"></a>Members

 **ulbLpszLabel**
  
> ボタンに表示される文字の文字列のメモリ内の位置。
    
 **ulFlags**
  
> **UlbLpszLabel**メンバーで指定されたラベルの書式を指定するために使用するフラグのビットマスクです。 次のフラグを設定することができます。 
    
MAPI_UNICODE 
  
> ラベルは、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式のラベルです。
    
 **ulPRControl**
  
> PT_OBJECT [IMAPIControl](imapicontroliunknown.md)インターフェイスを実装する種類のプロパティのプロパティ タグです。 ボタンをクリックすると、MAPI は、このプロパティを取得するために表示された表の[IMAPIProp](imapipropiunknown.md)の実装の[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出します。 
    
## <a name="remarks"></a>注釈

ボタン コントロールを記述する**DTBLBUTTON**構造体をクリックすると、操作を開始するユーザーに許可します。 通常、ボタンをクリックすると、表示されるモーダル ダイアログ ボックスまたはプログラムのタスクが呼び出されます。 サービス プロバイダーには、ボタン コントロールで何かを実装できます。 ボタンは、他のコントロールの値に基づいてタスクを実行することになって場合、それらのコントロールが、DT_SET_IMMEDIATE フラグを設定した必要があります。 
  
**UlbLpszLabel**メンバーは、ボタンに表示される文字の文字列のメモリ内の位置です。 サービス プロバイダーは、アンパサンド文字を追加できます (&amp;) ボタンのラベルのウィンドウのアクセラレータを指定します。 アクセラレータ キーを押すとボタンをクリックすると同じ効果を持ちます。 
  
**UlPRControl**メンバーは、オブジェクトのプロパティを記述する、 **IMAPIProp::OpenProperty**メソッドを使用する開くと、コントロール オブジェクトへのポインターを返します。 **IMAPIControl**インターフェイスをサポートするコントロール オブジェクトを実装するは、MAPI 機能を拡張し、ボタンがクリックされたときに発生するタスクまたは操作を定義する方法です。 **IMAPIControl**ボタンを操作するための 2 つの方法を提供する: ボタンとボタンのクリックを処理するために[アクティブ化](imapicontrol-activate.md)を有効または無効にするのには、 [GetState](imapicontrol-getstate.md) 。 
  
テーブルの表示の概要については、[テーブルの表示](display-tables.md)を参照してください。 表示テーブルを実装する方法の詳細については、[表示テーブルを実装する](display-table-implementation.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[DTCTL](dtctl.md)


[MAPI の構造](mapi-structures.md)

