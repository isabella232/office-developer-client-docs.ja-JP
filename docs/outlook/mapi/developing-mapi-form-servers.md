---
title: MAPI フォームサーバーの開発
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30672a2d-2d39-4292-b21a-97a38485d1de
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 63aa9db19c901f47004a7fe52d906846f44b8883
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338529"
---
# <a name="developing-mapi-form-servers"></a>MAPI フォームサーバーの開発

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
このセクションでは、カスタム MAPI フォームを作成するためのフォームサーバー実行可能ファイルとフォーム構成ファイルを作成するプロセスについて説明します。 このセクションを読む前に、 [MAPI フォーム](mapi-forms.md)の情報について理解しておく必要があります。
  
フォームサーバーの開発には、次の手順が含まれます。
  
1. フォームに含める情報を決定し、その情報を保持する一連のプロパティを選択します。 詳細については、「[フォームのプロパティセットを選択する](choosing-a-form-s-property-set.md)」を参照してください。
    
2. ユーザーがフォームのプロパティを操作できるユーザーインターフェイスの設計。
    
3. メッセージクラスを選択し、一意のクラス識別子 (CLSID) を生成します。 メッセージクラスの概要については、「 [MAPI メッセージクラス](mapi-message-classes.md)」を参照してください。 メッセージクラスとフォームの詳細については、「[メッセージクラスの選択](choosing-a-message-class.md)」を参照してください。
    
4. 必要な MAPI フォームインターフェイス、および特定のフォームサーバーが必要とする任意のインターフェイスを実装します。 詳細については、「[フォームサーバーコードを作成](writing-form-server-code.md)する」を参照してください。 
    
5. ユーザーが form オブジェクトとの対話およびフォームで使用するプロパティを処理するためのユーザーインターフェイスコードを記述します。
    
6. フォーム用のフォーム構成ファイルを作成します。 詳細については、「[フォーム構成ファイルのファイル形式](file-format-of-form-configuration-files.md)」を参照してください。
    
7. ユーザーのコンピューターへのフォームのインストール。 詳細については、「[ライブラリへのフォームのインストール](installing-a-form-into-a-library.md)」を参照してください。
    
多くの場合、手順 1 ~ 5 は順番に完了するのではなく、同時に実行します。 多くのプログラミングプロジェクトと同様に、フォームサーバーを開発するプロセスは、特に明確に定義されたシーケンスが存在するものではありません。 たとえば、フォーム構成ファイルの作成は、上記の2番目の手順として示されていますが、フォーム構成ファイルは段階的に作成することが多く、フォームサーバーに機能を追加するとより完全になります。
  
## <a name="see-also"></a>関連項目



[MAPI の概念](mapi-concepts.md)

