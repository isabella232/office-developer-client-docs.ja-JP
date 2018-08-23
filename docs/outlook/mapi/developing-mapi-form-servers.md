---
title: MAPI フォーム サーバーの開発
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30672a2d-2d39-4292-b21a-97a38485d1de
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 83d652f313e139b1c6bb628d1119edda03a70e23
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799920"
---
# <a name="developing-mapi-form-servers"></a>MAPI フォーム サーバーの開発

  
  
**適用対象**: Outlook 
  
このセクションでは、フォーム サーバーの実行可能ファイルとカスタム MAPI フォームを作成するためのフォーム構成ファイルを作成するプロセスについて説明します。 このセクションを読む前にする必要があります理解する[MAPI フォーム](mapi-forms.md)内の情報です。
  
フォームのサーバーを開発すると、次の手順が含まれています。
  
1. フォームに含まれるどのような情報を決定して、その情報を保持するプロパティのセットを選択します。 詳細については、[フォームのプロパティの設定を選択する](choosing-a-form-s-property-set.md)を参照してください。
    
2. フォームのプロパティを持つユーザーが対話するユーザー インターフェイスを設計しています。
    
3. メッセージ クラスを選択し、一意のクラス識別子 (CLSID) を生成しています。 メッセージ クラスの概要については、 [MAPI メッセージ クラス](mapi-message-classes.md)を参照してください。 メッセージ クラスおよびフォームの詳細については、[メッセージ クラスを選択する](choosing-a-message-class.md)を参照してください。
    
4. MAPI フォームの必要なインターフェイスと同様、特定のフォームのサーバーが必要なすべての省略可能なインターフェイスを実装します。 詳細については、[フォーム サーバー コードの記述](writing-form-server-code.md)を参照してください。 
    
5. フォームを使用フォームのオブジェクトとプロパティを持つユーザーの相互作用を処理するためにユーザー インターフェイスのコードを記述します。
    
6. フォームのフォーム構成ファイルを作成します。 詳細については、[フォーム構成ファイルの形式のファイル](file-format-of-form-configuration-files.md)を参照してください。
    
7. フォームをユーザーのコンピューターにインストールします。 詳細については、[ライブラリにフォームをインストールする](installing-a-form-into-a-library.md)を参照してください。
    
手順 1 ~ 5 はほとんどの場合、シーケンスで実行するのではなく、同時にします。 多くのプログラミング プロジェクトと同様に、フォームのサーバーの開発プロセスは、いずれかのでは、特に明確に定義されたシーケンスではありません。 たとえば、フォーム構成ファイルを作成するのようと、最後に 2 番目のステップですが、段階的に、フォーム構成ファイルを作成するが可能性があります、フォームのサーバーに機能を追加するときに詳細になります。
  
## <a name="see-also"></a>関連項目



[MAPI の概念](mapi-concepts.md)

