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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: fbe6dc9364ee953661d574b70bcd225abcfe7a81
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413060"
---
# <a name="imapiformmgr--iunknown"></a>IMAPIFormMgr : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォーム ビューアーがフォーム サーバーに関する情報を取得し、アクティブ化できます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform.h  <br/> |
|次のユーザーによって公開されます。  <br/> |フォーム マネージャー オブジェクト  <br/> |
|実装元:  <br/> |フォーム ライブラリ プロバイダー  <br/> |
|呼び出し元:  <br/> |フォーム ビューアー  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPIFormMgr  <br/> |
|ポインターの種類:  <br/> |LPMAPIFORMMGR  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[LoadForm](imapiformmgr-loadform.md) <br/> |既存のメッセージを開くフォームを開始します。  <br/> |
|[ResolveMessageClass](imapiformmgr-resolvemessageclass.md) <br/> |メッセージ クラスをフォーム コンテナー内のフォームに解決し、そのフォームのフォーム情報オブジェクトを返します。  <br/> |
|[ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md) <br/> |メッセージ クラスのグループをフォーム コンテナー内のフォームに解決し、それらのフォームのフォーム情報オブジェクトの配列を返します。  <br/> |
|[CalcFormPropSet](imapiformmgr-calcformpropset.md) <br/> |フォームのグループが使用するプロパティの配列を返します。  <br/> |
|[CreateForm](imapiformmgr-createform.md) <br/> |フォームを起動して、フォームのメッセージ クラスに基づいて新しいメッセージを作成します。  <br/> |
|[SelectForm](imapiformmgr-selectform.md) <br/> |ユーザーがフォームを選択できるダイアログ ボックスを表示し、そのフォームを説明するフォーム情報オブジェクトを返します。  <br/> |
|[SelectMultipleForms](imapiformmgr-selectmultipleforms.md) <br/> |ユーザーが複数のフォームを選択できるダイアログ ボックスを表示し、それらのフォームを記述するフォーム情報オブジェクトの配列を返します。  <br/> |
|[SelectFormContainer](imapiformmgr-selectformcontainer.md) <br/> |ユーザーがフォーム コンテナーを選択できるダイアログ ボックスを表示し、ユーザーが選択したコンテナー オブジェクトのインターフェイスを返します。  <br/> |
|[OpenFormContainer](imapiformmgr-openformcontainer.md) <br/> |特定の [フォーム コンテナーの IMAPIFormContainer](imapiformcontaineriunknown.md) インターフェイスを開きます。  <br/> |
|[PrepareForm](imapiformmgr-prepareform.md) <br/> |開くフォームをダウンロードします。  <br/> |
|[IsInConflict](imapiformmgr-isinconflict.md) <br/> |フォームが独自のメッセージ競合を処理できるかどうかを決定します。  <br/> |
|[GetLastError](imapiformmgr-getlasterror.md) <br/> |フォーム マネージャー オブジェクトに発生した以前のエラーに関する情報を含む [MAPIERROR](mapierror.md) 構造体を返します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

