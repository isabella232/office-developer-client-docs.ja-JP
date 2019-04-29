---
title: MAPI フォームオブジェクト
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
# <a name="mapi-form-objects"></a>MAPI フォームオブジェクト

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームオブジェクトは、フォームサーバーによって動的に作成され、特定のメッセージを表示したり、ユーザーがそれらを操作したりできるようになります。 そのため、form オブジェクトは、フォームサーバーによって実装されている[imapiform](imapiformiunknown.md)から派生したクラスのインスタンス化を行います。 クライアントアプリケーションがメッセージを開くと、そのメッセージクラスのフォームサーバーがメッセージを処理するためのフォームオブジェクトを作成します。 その後、form オブジェクトはそのインターフェイスを作成し、メッセージのプロパティを表示します。 form オブジェクトとそのインターフェイスは、ユーザーがそれを閉じるまで保持されます。 form オブジェクトは、メッセージのプロパティの値に対するすべての変更を処理します。 
  
さらに、MAPI フォームインターフェイスは、1つの form オブジェクトが一連のメッセージを読み込んで表示できるメカニズムを定義します。 これは、不必要な消滅や、メッセージオブジェクトとそのインターフェイスの作成を回避することで、効率のメカニズムです。 別のメッセージを読み込むために、メッセージングクライアントによって要求された場合、form オブジェクトは現在のメッセージのプロパティに対する変更を保存する必要があります。
  
クライアントアプリケーションによるフォームオブジェクトの視点については、「 [MAPI カスタムフォームオブジェクト](mapi-custom-form-objects.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[MAPI フォーム](mapi-forms.md)

