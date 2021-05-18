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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a8fa683fecd59ec813fee0c15d5b4f08084c645d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412787"
---
# <a name="dtblbutton"></a>DTBLBUTTON

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
表示テーブルから作成されたダイアログ ボックスのボタン コントロールに関する情報を格納します。
  
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
  
> ボタンに表示される文字列のメモリ内の位置。
    
 **ulFlags**
  
> **ulbLpszLabel** メンバーが指すラベルの形式を指定するために使用されるフラグのビットマスク。 次のフラグを設定できます。 
    
MAPI_UNICODE 
  
> ラベルは Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、ラベルは ANSI 形式になります。
    
 **ulPRControl**
  
> [IMAPIControl](imapicontroliunknown.md)インターフェイスを実装するPT_OBJECTのプロパティ タグ。 ボタンをクリックすると、MAPI は表示テーブルの IMAPIProp 実装の[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出して、このプロパティを取得します。 [](imapipropiunknown.md) 
    
## <a name="remarks"></a>注釈

**DTBLBUTTON 構造体は**、ボタンをクリックすると、ユーザーが操作を開始できるコントロールを表します。 通常、ボタンをクリックすると、モーダル ダイアログ ボックスが表示される、またはプログラムによるタスクが呼び出されます。 サービス プロバイダーは、ボタン コントロールを通じて何でも実装できます。 ボタンが他のコントロールの値に基づいてタスクを実行する必要がある場合は、これらのコントロールでタスク フラグDT_SET_IMMEDIATEがあります。 
  
**ulbLpszLabel** メンバーは、ボタンに表示される文字列のメモリ内の位置です。 サービス プロバイダーは、アンパサンド文字 ( ) を追加して、ボタン ラベルにWindows &amp; アクセラレータを示します。 アクセラレータ キーを押すと、ボタンをクリックした場合と同じ効果が得られます。 
  
**ulPRControl** メンバーは **、IMAPIProp::OpenProperty** メソッドで開いた場合に、コントロール オブジェクトへのポインターを返すオブジェクト プロパティを表します。 **IMAPIControl** インターフェイスをサポートするコントロール オブジェクトを実装すると、MAPI 機能セットを拡張し、ボタンをクリックするときに発生する操作またはタスクを定義できます。 **IMAPIControl には** 、ボタンを操作するための 2 つのメソッドが提供されています。ボタンを無効または有効にする [GetState](imapicontrol-getstate.md) と、ボタンのクリックを処理するための [アクティブ](imapicontrol-activate.md) 化。 
  
表示テーブルの概要については、「表示テーブル」 [を参照してください](display-tables.md)。 表示テーブルを実装する方法の詳細については、「表示テーブルの [実装」を参照してください](display-table-implementation.md)。
  
## <a name="see-also"></a>関連項目



[DTCTL](dtctl.md)


[MAPI の構造](mapi-structures.md)

