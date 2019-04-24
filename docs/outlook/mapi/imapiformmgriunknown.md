---
title: imapiformmgr IUnknown
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
ms.openlocfilehash: fbe6dc9364ee953661d574b70bcd225abcfe7a81
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321652"
---
# <a name="imapiformmgr--iunknown"></a>IMAPIFormMgr : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームビューアーがフォームサーバーに関する情報を取得し、アクティブ化できるようにします。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform  <br/> |
|公開者:  <br/> |フォームマネージャーオブジェクト  <br/> |
|実装元:  <br/> |フォームライブラリプロバイダー  <br/> |
|呼び出し元:  <br/> |フォームビューアー  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPIFormMgr  <br/> |
|ポインターの種類:  <br/> |LPMAPIFORMMGR  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[loadform](imapiformmgr-loadform.md) <br/> |既存のメッセージを開くフォームを開始します。  <br/> |
|[ResolveMessageClass](imapiformmgr-resolvemessageclass.md) <br/> |form コンテナー内のフォームに対してメッセージクラスを解決し、そのフォームのフォーム情報オブジェクトを返します。  <br/> |
|[ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md) <br/> |フォームコンテナー内のフォームに対するメッセージクラスのグループを解決し、それらのフォームのフォーム情報オブジェクトの配列を返します。  <br/> |
|[CalcFormPropSet](imapiformmgr-calcformpropset.md) <br/> |フォームのグループが使用するプロパティの配列を返します。  <br/> |
|[CreateForm](imapiformmgr-createform.md) <br/> |フォームのメッセージクラスに基づいて新しいメッセージを作成するためのフォームを起動します。  <br/> |
|[selectform](imapiformmgr-selectform.md) <br/> |ユーザーがフォームを選択できるようにするダイアログボックスを表示し、そのフォームを記述するフォーム情報オブジェクトを返します。  <br/> |
|[select多重フォーム](imapiformmgr-selectmultipleforms.md) <br/> |ユーザーが複数のフォームを選択できるようにするダイアログボックスを表示し、それらのフォームを記述するフォーム情報オブジェクトの配列を返します。  <br/> |
|[selectformcontainer](imapiformmgr-selectformcontainer.md) <br/> |ユーザーがフォームコンテナーを選択できるようにするダイアログボックスを提供し、ユーザーが選択したコンテナーオブジェクトのインターフェイスを返します。  <br/> |
|[openformcontainer](imapiformmgr-openformcontainer.md) <br/> |特定のフォームコンテナーの[imapiformcontainer](imapiformcontaineriunknown.md)インターフェイスを開きます。  <br/> |
|[PrepareForm](imapiformmgr-prepareform.md) <br/> |開くフォームをダウンロードします。  <br/> |
|[IsInConflict](imapiformmgr-isinconflict.md) <br/> |フォームが独自のメッセージ競合を処理できるかどうかを決定します。  <br/> |
|[GetLastError](imapiformmgr-getlasterror.md) <br/> |フォームマネージャーオブジェクトに発生する前のエラーについての情報を含む[MAPIERROR](mapierror.md)構造体を返します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

