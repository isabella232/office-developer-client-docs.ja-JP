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
ms.openlocfilehash: 8dce1415ef8d18f4b786e92324c888f9a0845162
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280142"
---
# <a name="imapicontrol--iunknown"></a>IMAPIControl : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ボタンコントロールを有効または無効にし、クライアントアプリケーションのユーザーが有効になっているコントロールをクリックしたときにタスクを実行します。 サービスプロバイダーは、コントロールオブジェクトを実装して、表示テーブルを使用して定義される構成プロパティシートなどのカスタムボタンをダイアログボックスに作成します。 
  
表示テーブルとコントロールオブジェクトを操作する方法の詳細については、「[表を表示](display-tables.md)する」を参照してください。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|公開者:  <br/> |Control オブジェクト  <br/> |
|実装元:  <br/> |サービス プロバイダー  <br/> |
|呼び出し元:  <br/> |MAPI  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPIControl  <br/> |
|ポインターの種類:  <br/> |LPMAPICONTROL  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[GetLastError](imapicontrol-getlasterror.md) <br/> |前のボタンコントロールのエラーについての情報を含む[MAPIERROR](mapierror.md)構造体を返します。  <br/> |
|[Activate](imapicontrol-activate.md) <br/> |クライアントアプリケーションユーザーが [ボタン] コントロールをクリックしたときに、ダイアログボックスを表示したり、プログラムによる操作を開始したりするなどのタスクを実行します。  <br/> |
|[GetState](imapicontrol-getstate.md) <br/> |ボタンコントロールが有効であるか無効であるかを示す値を取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

