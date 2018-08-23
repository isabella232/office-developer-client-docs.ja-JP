---
title: IMAPIFormMgr IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr
api_type:
- COM
ms.assetid: 8cbd1a42-7de6-43e0-8c77-7711773843d5
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b4eaf424bd22f5cb7f40778d81a18cca0ef1dcc1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581518"
---
# <a name="imapiformmgr--iunknown"></a>IMAPIFormMgr : IUnknown

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
フォームの閲覧者に関する情報を取得し、フォームのサーバーをアクティブ化を有効にします。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform.h  <br/> |
|によって公開されます。  <br/> |フォーム マネージャー オブジェクト  <br/> |
|によって実装されます。  <br/> |フォーム ライブラリのプロバイダー  <br/> |
|によって呼び出されます。  <br/> |フォームの閲覧者  <br/> |
|インターフェイスの識別子。  <br/> |IID_IMAPIFormMgr  <br/> |
|ポインターの型。  <br/> |LPMAPIFORMMGR  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[LoadForm](imapiformmgr-loadform.md) <br/> |フォームを開くには既存のメッセージを開始します。  <br/> |
|[ResolveMessageClass](imapiformmgr-resolvemessageclass.md) <br/> |フォームのコンテナー内のフォームにメッセージ クラスを解決し、そのフォームのフォームについてはオブジェクトを取得します。  <br/> |
|[ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md) <br/> |フォームのコンテナー内でユーザーがフォームにメッセージ クラスのグループを解決し、それらのフォームのオブジェクトの情報、フォームの配列を返します。  <br/> |
|[CalcFormPropSet](imapiformmgr-calcformpropset.md) <br/> |フォームのグループを使用するプロパティの配列を返します。  <br/> |
|[CreateForm](imapiformmgr-createform.md) <br/> |フォームのメッセージ クラスに基づく新しいメッセージを作成するためのフォームを起動します。  <br/> |
|[SelectForm](imapiformmgr-selectform.md) <br/> |、フォームを選択するユーザーを有効にする] ダイアログ ボックスを表示し、そのフォームを記述するフォームの情報オブジェクトを返します。  <br/> |
|[SelectMultipleForms](imapiformmgr-selectmultipleforms.md) <br/> |複数のフォームを選択するユーザーを有効にする] ダイアログ ボックスを表示し、それらのフォームを記述するオブジェクトの情報、フォームの配列を返します。  <br/> |
|[SelectFormContainer](imapiformmgr-selectformcontainer.md) <br/> |により、ユーザーがフォームのコンテナーを選択し、ユーザーが選択したコンテナーのオブジェクトのインターフェイスを返しますダイアログ ボックスが表示されます。  <br/> |
|[OpenFormContainer](imapiformmgr-openformcontainer.md) <br/> |[IMAPIFormContainer](imapiformcontaineriunknown.md)インターフェイスの特定のフォームのコンテナーを開きます。  <br/> |
|[PrepareForm](imapiformmgr-prepareform.md) <br/> |開始するためのフォームをダウンロードします。  <br/> |
|[IsInConflict](imapiformmgr-isinconflict.md) <br/> |フォームに独自のメッセージの競合を処理できるかどうかを決定します。  <br/> |
|[発生しました](imapiformmgr-getlasterror.md) <br/> |フォーム マネージャー オブジェクトに発生する前のエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI インターフェイス](mapi-interfaces.md)

