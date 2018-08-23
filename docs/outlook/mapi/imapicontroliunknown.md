---
title: IMAPIControl IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl
api_type:
- COM
ms.assetid: 5a647e15-ba22-4a7c-b235-75cd76b77c1a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 395e44c2ea54816fab9f29dbedfe5e165e98c7b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800453"
---
# <a name="imapicontrol--iunknown"></a>IMAPIControl : IUnknown

  
  
**適用対象**: Outlook 
  
ボタン コントロールを無効にでき、クライアント アプリケーションのユーザーが有効なコントロールをクリックしたときにタスクを実行します。 サービス プロバイダーは、設定プロパティ シートの表示のテーブルを使用して定義されているなどのダイアログ ボックスにカスタム ボタンを作成するコントロール オブジェクトを実装します。 
  
表示のテーブルを操作し、オブジェクトを制御する方法の詳細については、[テーブルの表示](display-tables.md)を参照してください。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|によって公開されます。  <br/> |コントロール オブジェクト  <br/> |
|によって実装されます。  <br/> |サービス プロバイダー  <br/> |
|によって呼び出されます。  <br/> |MAPI  <br/> |
|インターフェイスの識別子。  <br/> |IID_IMAPIControl  <br/> |
|ポインターの型。  <br/> |LPMAPICONTROL  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[発生しました](imapicontrol-getlasterror.md) <br/> |前のボタン コントロールのエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。  <br/> |
|[Activate](imapicontrol-activate.md) <br/> |ダイアログ ボックスを表示する、クライアント アプリケーションのユーザーは、ボタン コントロールをクリックすると、プログラムの操作を開始するなどのタスクを実行します。  <br/> |
|[GetState](imapicontrol-getstate.md) <br/> |ボタン コントロールを有効または無効にするかどうかを示す値を取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI インターフェイス](mapi-interfaces.md)

