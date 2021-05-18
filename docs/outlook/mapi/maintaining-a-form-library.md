---
title: フォーム ライブラリの保守
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8488f7ec-e44b-4d1a-ba42-baea8c71d350
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 51c7c3f8ba70dcb3d35dc50806e984fd4b193818
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408804"
---
# <a name="maintaining-a-form-library"></a>フォーム ライブラリの保守

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォーム ライブラリには、フォームのプロパティ、動詞、サーバーの実行可能ファイルなど、フォームに関する重要な情報すべてが保持されます。 一部のクライアントでは、ユーザーがフォーム サーバーを保守、インストール、または削除できます。 この機能をユーザーに提供する場合は、次の機能にアクセスできる必要があります。
  
- フォーム サーバーの構成ファイル、.CFG 拡張機能。
    
- フォーム ライブラリのコンテナー オブジェクト [、IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md) インターフェイスを実装するオブジェクト。 
    
構成ファイルまたはパス名にアクセスするには、便利な手段を使用します。 通常、クライアントは、構成ファイルの場所をユーザーに確認するフォーム サーバーをインストールおよび削除するためのダイアログ ボックスをユーザーに表示します。
  
フォーム ライブラリのコンテナーにアクセスするには、フォーム マネージャーの [IMAPIFormMgr::OpenFormContainer メソッドを呼び出](imapiformmgr-openformcontainer.md) します。 列挙値を渡して、開くフォーム ライブラリを指定し、必要に応じてフォーム マネージャーがフォーム ライブラリを開くのに使用するオブジェクトへのポインターを指定します。 たとえば、フォルダー フォーム ライブラリを[](folder-form-libraries.md)開く場合は[、IMAPIFolder : IMAPIContainer ポインターを渡](imapifolderimapicontainer.md)します。 
  
**OpenFormContainer** が **IMAPIFormContainer** ポインターを返した後、実行するメンテナンスに応じて [、IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md)または [IMAPIFormContainer::RemoveForm](imapiformcontainer-removeform.md)を呼び出します。 **InstallForm** は、フォーム サーバーをライブラリに追加します。 **RemoveForm** は、フォーム サーバーをライブラリから削除します。 
  

