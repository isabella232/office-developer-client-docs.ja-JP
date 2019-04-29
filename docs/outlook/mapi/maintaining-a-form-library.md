---
title: フォームライブラリの管理
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
# <a name="maintaining-a-form-library"></a>フォームライブラリの管理

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームライブラリには、フォームに関する重要な情報がすべて含まれます。フォームのプロパティ、動詞、およびサーバーの実行可能ファイル。 クライアントによっては、フォームサーバーの保守、インストール、または削除をユーザーに許可することができます。 この機能をユーザーに提供するには、次のものにアクセスできる必要があります。
  
- フォームサーバーの構成ファイル。このファイルには、が含まれます。CFG 拡張機能。
    
- フォームライブラリの container オブジェクト[。 imapiformcontainer: IUnknown](imapiformcontaineriunknown.md)インターフェイスを実装するオブジェクト。 
    
構成ファイルまたはパス名にアクセスするには、任意の方法を使用します。 通常、クライアントは、ユーザーに対してフォームサーバーをインストールおよび削除するためのダイアログボックスを表示します。このダイアログボックスを使用すると、構成ファイルの場所をユーザーに確認することもできます。
  
フォームライブラリのコンテナーにアクセスするには、フォームマネージャーの[imapiformmgr:: openformcontainer](imapiformmgr-openformcontainer.md)メソッドを呼び出します。 開くフォームライブラリを指定する列挙値を渡し、必要に応じて、フォームマネージャーがフォームライブラリを開くために使用するオブジェクトへのポインターを指定します。 たとえば、[フォルダーフォームライブラリ](folder-form-libraries.md)を開く場合は、 [imapifolder: IMAPIContainer](imapifolderimapicontainer.md)ポインターを渡します。 
  
**openformcontainer**が**imapiformcontainer**ポインターを返すと、実行するメンテナンスに応じて、 [imapiformcontainer:: installform](imapiformcontainer-installform.md)または[imapiformcontainer:: removeform](imapiformcontainer-removeform.md)のいずれかを呼び出します。 **installform**は、フォームサーバーをライブラリに追加します。**removeform**ライブラリからフォームサーバーを削除します。 
  

