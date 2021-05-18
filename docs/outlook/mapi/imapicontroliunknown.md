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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8dce1415ef8d18f4b786e92324c888f9a0845162
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414040"
---
# <a name="imapicontrol--iunknown"></a>IMAPIControl : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ボタン コントロールを有効または無効にし、クライアント アプリケーションのユーザーが有効なコントロールをクリックするとタスクを実行します。 サービス プロバイダーは、表示テーブルを使用して定義された構成プロパティ シートなどのダイアログ ボックスにカスタム ボタンを作成するコントロール オブジェクトを実装します。 
  
表示テーブルとコントロール オブジェクトを操作する方法の詳細については、「Display Tables 」を [参照してください](display-tables.md)。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|次のユーザーによって公開されます。  <br/> |コントロール オブジェクト  <br/> |
|実装元:  <br/> |サービス プロバイダー  <br/> |
|呼び出し元:  <br/> |MAPI  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPIControl  <br/> |
|ポインターの種類:  <br/> |LPMAPICONTROL  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[GetLastError](imapicontrol-getlasterror.md) <br/> |前のボタン コントロール エラーに関する情報を含む [MAPIERROR](mapierror.md) 構造体を返します。  <br/> |
|[Activate](imapicontrol-activate.md) <br/> |クライアント アプリケーション のユーザーがボタン コントロールをクリックすると、ダイアログ ボックスの表示やプログラムによる操作の開始などのタスクを実行します。  <br/> |
|[GetState](imapicontrol-getstate.md) <br/> |ボタン コントロールが有効か無効かを示す値を取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

