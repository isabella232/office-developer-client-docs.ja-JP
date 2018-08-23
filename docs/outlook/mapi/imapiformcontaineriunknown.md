---
title: IMAPIFormContainer IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer
api_type:
- COM
ms.assetid: 437c8a75-1121-4919-8bd4-d57c0d6f4b9a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3f03412c9ab639678c68016ec1a8eff937b6c1a0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590989"
---
# <a name="imapiformcontainer--iunknown"></a>IMAPIFormContainer : IUnknown

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
フォーム ライブラリにフォームを管理します。 このインターフェイスを使用して、アプリケーション固有のフォーム ライブラリを作成できます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform.h  <br/> |
|によって公開されます。  <br/> |フォームのコンテナー オブジェクト  <br/> |
|によって実装されます。  <br/> |フォーム ライブラリのプロバイダー  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーション  <br/> |
|インターフェイスの識別子。  <br/> |IID_IMAPIFormContainer  <br/> |
|ポインターの型。  <br/> |LPMAPIFORMCONTAINER  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[InstallForm](imapiformcontainer-installform.md) <br/> |フォームのコンテナーには、フォームをインストールします。  <br/> |
|[RemoveForm](imapiformcontainer-removeform.md) <br/> |特定のフォームは、フォームのコンテナーから削除します。  <br/> |
|[ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) <br/> |フォームのコンテナー内のフォームにメッセージ クラスを解決し、そのフォームのフォームについてはオブジェクトを取得します。  <br/> |
|[ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md) <br/> |フォームのコンテナー内のフォームにメッセージ クラスのグループを解決し、それらのフォームのオブジェクトの情報、フォームの配列を返します。  <br/> |
|[CalcFormPropSet](imapiformcontainer-calcformpropset.md) <br/> |フォームのコンテナーにインストールされているすべてのフォームで使用されるプロパティの配列を返します。  <br/> |
|[GetDisplay](imapiformcontainer-getdisplay.md) <br/> |フォームのコンテナーの表示名を返します。  <br/> |
|[発生しました](imapiformcontainer-getlasterror.md) <br/> |フォームのコンテナー オブジェクトに発生する前のエラーに関する情報を含む[MAPIERROR](mapierror.md)構造体を返します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI インターフェイス](mapi-interfaces.md)

