---
title: MAPI フォーム オブジェクト
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb9107d9-ad5c-4264-a457-dea193597dc9
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 0cece598d4ad337e29edb3bb98b302de900e056d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593467"
---
# <a name="mapi-form-objects"></a>MAPI フォーム オブジェクト

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
フォーム オブジェクトは、特定のメッセージを表示し、それらと対話できるようにするためにフォームのサーバーによって動的に作成されます。 フォーム オブジェクトは、フォーム サーバーが実装されている[IMAPIForm](imapiformiunknown.md)から派生したクラスのインスタンス化します。 クライアント アプリケーションは、メッセージを開き、そのメッセージ クラスのフォームのサーバーは、メッセージを処理するフォーム オブジェクトを作成します。 フォーム オブジェクトは、そのインタ フェースを作成し、メッセージのプロパティを表示します。 フォーム オブジェクトとそのインタ フェースは、ユーザーが閉じるまでに永続化されます。 フォーム オブジェクトは、メッセージのプロパティの値への変更を処理します。 
  
さらに、MAPI フォームのインタ フェースは、1 つのフォーム オブジェクトを読み込むし、一連のメッセージを表示する機構を定義します。 これは、言うまでもなく破壊し、メッセージのオブジェクトとそのインターフェイスの作成を回避できるので、効率性のメカニズムです。 メッセージング クライアントによって要求されると別のメッセージをロードするのには、form オブジェクトは現在のメッセージのプロパティに変更を保存する必要があります。
  
フォーム オブジェクトのクライアント アプリケーションの観点については、 [MAPI ユーザー設定のフォーム オブジェクト](mapi-custom-form-objects.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[MAPI フォーム](mapi-forms.md)

