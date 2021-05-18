---
title: MAPI フォーム オブジェクト
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb9107d9-ad5c-4264-a457-dea193597dc9
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5a7c6c575f277a91a18f0d834e26d3d376613fba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404786"
---
# <a name="mapi-form-objects"></a>MAPI フォーム オブジェクト

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォーム オブジェクトは、特定のメッセージを表示し、ユーザーがそれらを操作するために、フォーム サーバーによって動的に作成されます。 したがって、フォーム オブジェクトは、フォーム サーバーによって実装される [IMAPIForm](imapiformiunknown.md) から派生したクラスのインスタンス化です。 クライアント アプリケーションがメッセージを開くと、そのメッセージ クラスのフォーム サーバーによって、メッセージを処理するフォーム オブジェクトが作成されます。 フォーム オブジェクトは、そのインターフェイスを作成し、その中にメッセージのプロパティを表示します。 フォーム オブジェクトとそのインターフェイスは、ユーザーが閉じるまで保持されます。 フォーム オブジェクトは、メッセージのプロパティの値に対する変更を処理します。 
  
さらに、MAPI フォーム インターフェイスは、1 つのフォーム オブジェクトが一連のメッセージを読み込み、表示できるメカニズムを定義します。 これは、メッセージ オブジェクトとそのインターフェイスの不必要な破棄と作成を回避する効率メカニズムです。 メッセージング クライアントから別のメッセージの読み込みを要求された場合、フォーム オブジェクトは現在のメッセージのプロパティに対する変更を保存する必要があります。
  
クライアント アプリケーションのフォーム オブジェクトの観点については、「MAPI カスタム フォーム オブジェクト」 [を参照してください](mapi-custom-form-objects.md)。
  
## <a name="see-also"></a>関連項目



[MAPI フォーム](mapi-forms.md)

