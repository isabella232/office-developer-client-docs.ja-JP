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
ms.openlocfilehash: a8fa683fecd59ec813fee0c15d5b4f08084c645d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338312"
---
# <a name="dtblbutton"></a>DTBLBUTTON

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
表示テーブルから作成されたダイアログボックスのボタンコントロールに関する情報を格納します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
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

 **ulblpszlabel**
  
> ボタンに表示される文字列のメモリ内での位置を指定します。
    
 **ulFlags**
  
> **ulblpszlabel**メンバーが指すラベルの形式を指定するために使用されるフラグのビットマスク。 次のフラグを設定できます。 
    
MAPI_UNICODE 
  
> ラベルは Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、ラベルは ANSI 形式になります。
    
 **ulprcontrol**
  
> [IMAPIControl](imapicontroliunknown.md)インターフェイスを実装する PT_OBJECT 型のプロパティのプロパティタグ。 ボタンがクリックされると、MAPI は、表示テーブルの[imapiprop](imapipropiunknown.md)実装に対して[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを呼び出し、このプロパティを取得します。 
    
## <a name="remarks"></a>解説

**dtblbutton**構造体は、ボタンをクリックすると、ユーザーが操作を開始できるようにするコントロールを記述します。 通常、ボタンをクリックすると、モーダルダイアログボックスが表示されるか、プログラムによってタスクが呼び出されます。 サービスプロバイダーは、ボタンコントロールを使用して任意のものを実装できます。 他のコントロールの値に基づいてタスクを実行するようにボタンが設定されている場合、これらのコントロールでは DT_SET_IMMEDIATE フラグが設定されている必要があります。 
  
**ulblpszlabel**メンバーは、ボタンに表示される文字列のメモリ内の位置を示します。 サービスプロバイダーは、ボタンのラベルで&amp;Windows accelerator を示すために、アンパサンド文字 () を追加することができます。 アクセラレータキーを押すと、ボタンをクリックした場合と同じ結果になります。 
  
**ulprcontrol**メンバーは、 **imapiprop:: openproperty**メソッドを使用して開かれたときに、コントロールオブジェクトへのポインターを取得するオブジェクトのプロパティを記述します。 **IMAPIControl**インターフェイスをサポートする control オブジェクトを実装することは、MAPI 機能セットを拡張し、ボタンがクリックされたときに実行する操作またはタスクを定義する方法です。 **IMAPIControl**では、ボタンを有効または無効にするための 2 [](imapicontrol-activate.md)つのメソッドと、ボタンのクリックを処理するための[GetState](imapicontrol-getstate.md)を提供します。 
  
表示テーブルの概要については、「[テーブルの表示](display-tables.md)」を参照してください。 表示テーブルを実装する方法については、「[表示テーブルを実装](display-table-implementation.md)する」を参照してください。
  
## <a name="see-also"></a>関連項目



[DTCTL](dtctl.md)


[MAPI の構造](mapi-structures.md)

