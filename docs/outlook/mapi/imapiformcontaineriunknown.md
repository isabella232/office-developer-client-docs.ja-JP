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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 208af28307a60615ecafda0992881c5df36aa56f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407530"
---
# <a name="imapiformcontainer--iunknown"></a>IMAPIFormContainer : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォーム ライブラリ内のフォームを管理します。 このインターフェイスは、アプリケーション固有のフォーム ライブラリを作成するために使用されます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform.h  <br/> |
|次のユーザーによって公開されます。  <br/> |フォーム コンテナー オブジェクト  <br/> |
|実装元:  <br/> |フォーム ライブラリ プロバイダー  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPIFormContainer  <br/> |
|ポインターの種類:  <br/> |LPMAPIFORMCONTAINER  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[InstallForm](imapiformcontainer-installform.md) <br/> |フォームコンテナーにフォームをインストールします。  <br/> |
|[RemoveForm](imapiformcontainer-removeform.md) <br/> |フォーム コンテナーから特定のフォームを削除します。  <br/> |
|[ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) <br/> |メッセージ クラスをフォーム コンテナー内のフォームに解決し、そのフォームのフォーム情報オブジェクトを返します。  <br/> |
|[ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md) <br/> |メッセージ クラスのグループをフォーム コンテナー内のフォームに解決し、それらのフォームのフォーム情報オブジェクトの配列を返します。  <br/> |
|[CalcFormPropSet](imapiformcontainer-calcformpropset.md) <br/> |フォーム コンテナーにインストールされているすべてのフォームで使用されるプロパティの配列を返します。  <br/> |
|[GetDisplay](imapiformcontainer-getdisplay.md) <br/> |フォーム コンテナーの表示名を返します。  <br/> |
|[GetLastError](imapiformcontainer-getlasterror.md) <br/> |フォーム コンテナー オブジェクトに発生した以前のエラーに関する情報を含む [MAPIERROR](mapierror.md) 構造体を返します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

