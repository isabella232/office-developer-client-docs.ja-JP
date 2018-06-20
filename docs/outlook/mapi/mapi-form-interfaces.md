---
title: MAPI フォームのインタ フェース
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 611213c9-e758-4366-b193-fc62181d3d1f
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 8452a6e49059dd0912f1efffef7e749afd6cdf6a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801358"
---
# <a name="mapi-form-interfaces"></a>MAPI フォームのインタ フェース

  
  
**適用されます**: Outlook 
  
MAPI では、フォームに関連する次のインタ フェースを定義します。
  
|**インターフェイス名**|**説明**|
|:-----|:-----|
|[IMAPIForm](imapiformiunknown.md) <br/> |フォーム オブジェクトを操作し、フォームのオブジェクトのコマンドを処理します。  <br/> |
|[IMAPIFormAdviseSink](imapiformadvisesinkiunknown.md) <br/> |フォーム オブジェクトが次のメッセージを処理することができ、フォーム オブジェクトの次または前の状態を変更するかどうかを決定します。  <br/> |
|[IMAPIFormContainer](imapiformcontaineriunknown.md) <br/> |インストール、アンインストール、および特定のフォームのコンテナーに対するフォーム サーバーの解像度をサポートしています。  <br/> |
|[IMAPIFormFactory](imapiformfactoryiunknown.md) <br/> |サーバーの構成可能な実行時のフォームの使用をサポートしています。  <br/> |
|[IMAPIFormInfo](imapiforminfoimapiprop.md) <br/> |メッセージ クラスに特有のプロパティを操作するクライアント アプリケーションを有効にします。  <br/> |
|[IMAPIFormMgr](imapiformmgriunknown.md) <br/> |フォームのサーバーに関する情報を取得するクライアント アプリケーション、フォームのサーバーをアクティブにでき、メッセージング システムでは、フォームのサーバーをインストールします。  <br/> |
|[IMAPIMessageSite](imapimessagesiteiunknown.md) <br/> |フォーム オブジェクトに関連付けられているメッセージを操作するために使用します。  <br/> |
|[IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) <br/> |フォーム オブジェクトでイベントが発生するクライアント アプリケーションに通知します。  <br/> |
|[IMAPIViewContext](imapiviewcontextiunknown.md) <br/> |フォーム オブジェクトで、次、前、および削除のコマンドに応答する場合に使用されます。  <br/> |
|[IPersistMessage](ipersistmessageiunknown.md) <br/> |保存、初期化、およびメッセージの記憶域との間に、フォーム オブジェクトを読み込むに使用されます。  <br/> |
   
MAPI フォームのインターフェイスのメソッドに関する詳細については、これらのインタ フェースのマニュアルを参照してください。 カスタム フォームを作成するためにすべての MAPI フォームのインターフェイスを実装する必要はありません。 フォーム自体は、 **IPersistMessage**、 **IMAPIForm**を実装し、インターフェイスを**IMAPIFormAdviseSink**ことのみ必要です。 また、それは**IMAPIFormFactory**と**IMAPIFormInfo**を実装することをお勧めします。 **IMAPIFormFactory**は、OLE に準拠するために便利ですし、 **IMAPIFormInfo**は、フォームの使用方法を適切に設計されたクライアント アプリケーションを有効にします。 
  
> [!NOTE]
> **IMAPIFormAdviseSink**は、厳密に言うと、省略可能なインターフェイスです。 ただし、フォーム サーバーに実装することを強くお勧めします。 このインターフェイスは、メッセージング クライアントと、フォームのサーバーとの間の効率的な相互作用に重要な特にいくつかのメッセージが、フォームのサーバーのメッセージ クラスの処理中にします。 
  
## <a name="see-also"></a>関連項目



[MAPI フォーム](mapi-forms.md)

