---
title: フォーム ライブラリを維持します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8488f7ec-e44b-4d1a-ba42-baea8c71d350
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 5ccb5a2881d3cef3ff21a106e7e9ea33e0aedd9e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801292"
---
# <a name="maintaining-a-form-library"></a>フォーム ライブラリを維持します。

  
  
**適用されます**: Outlook 
  
フォーム ライブラリを保持するすべてのフォームに関する重要な情報: プロパティ、動詞、およびそのサーバーの実行可能ファイルです。 何人かのように、管理、インストール、またはフォームのサーバーを削除します。 この機能をユーザーに提供する場合へのアクセスが必要です。
  
- フォーム サーバーの構成ファイル、ファイルをします。CFG 拡張子を付けています。
    
- フォーム ライブラリのコンテナーのオブジェクト、オブジェクトを実装する、 [IMAPIFormContainer: IUnknown](imapiformcontaineriunknown.md)インタ フェースです。 
    
構成ファイルまたはパス名を使用してアクセスするのにはなんらかの方法が便利です。 通常、クライアントのインストールと構成ファイルの場所をユーザーに確認するのにも使用できるフォームのサーバーを削除するためのダイアログ ボックスをユーザーに表示します。
  
フォーム ライブラリのコンテナーにアクセスするには、フォーム マネージャーの[IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md)メソッドを呼び出します。 開くには、フォーム ライブラリを指定する列挙値のパスと、必要に応じて、フォーム ライブラリを開くにフォーム マネージャーを使用する必要がありますオブジェクトへのポインター。 の[フォーム ライブラリのフォルダー](folder-form-libraries.md)を開いている場合を渡すなど、 [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)のポインター。 
  
**IMAPIFormContainer**ポインターが返されると、 **OpenFormContainer**によっては、保守を実行する[IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md)または[IMAPIFormContainer::RemoveForm](imapiformcontainer-removeform.md)のいずれかを呼び出します。 **InstallForm**フォームのサーバーをライブラリに追加します。**RemoveForm**は、フォームのサーバーをライブラリから削除します。 
  

