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
ms.openlocfilehash: 426d3d5787f4ef8cde2883c5e2eb3699dd664965
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801373"
---
# <a name="mapi-form-objects"></a>MAPI フォーム オブジェクト

  
  
**適用対象**: Outlook 
  
フォーム オブジェクトは、特定のメッセージを表示し、それらと対話できるようにするためにフォームのサーバーによって動的に作成されます。 フォーム オブジェクトは、フォーム サーバーが実装されている[IMAPIForm](imapiformiunknown.md)から派生したクラスのインスタンス化します。 クライアント アプリケーションは、メッセージを開き、そのメッセージ クラスのフォームのサーバーは、メッセージを処理するフォーム オブジェクトを作成します。 フォーム オブジェクトは、そのインタ フェースを作成し、メッセージのプロパティを表示します。 フォーム オブジェクトとそのインタ フェースは、ユーザーが閉じるまでに永続化されます。 フォーム オブジェクトは、メッセージのプロパティの値への変更を処理します。 
  
さらに、MAPI フォームのインタ フェースは、1 つのフォーム オブジェクトを読み込むし、一連のメッセージを表示する機構を定義します。 これは、言うまでもなく破壊し、メッセージのオブジェクトとそのインターフェイスの作成を回避できるので、効率性のメカニズムです。 メッセージング クライアントによって要求されると別のメッセージをロードするのには、form オブジェクトは現在のメッセージのプロパティに変更を保存する必要があります。
  
フォーム オブジェクトのクライアント アプリケーションの観点については、 [MAPI ユーザー設定のフォーム オブジェクト](mapi-custom-form-objects.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[MAPI フォーム](mapi-forms.md)

