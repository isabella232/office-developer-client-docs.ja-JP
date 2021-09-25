---
title: MAPI フォーム サーバーの開発
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 30672a2d-2d39-4292-b21a-97a38485d1de
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: af3960938defba5b14a602704ccd5a214951a6e0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605035"
---
# <a name="developing-mapi-form-servers"></a>MAPI フォーム サーバーの開発

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
このセクションでは、カスタム MAPI フォームを作成するためのフォーム サーバー実行可能ファイルとフォーム構成ファイルを作成するプロセスについて説明します。 このセクションを読む前に、MAPI フォームの情報を [理解する必要があります](mapi-forms.md)。
  
フォーム サーバーの開発には、次の手順が含まれます。
  
1. フォームに含まれる情報を決定し、その情報を保持する一連のプロパティを選択します。 詳細については、「フォームの [プロパティ セットの選択」を参照してください](choosing-a-form-s-property-set.md)。
    
2. ユーザーがフォームのプロパティを操作できるユーザー インターフェイスを設計する。
    
3. メッセージ クラスを選択し、一意のクラス識別子 (CLSID) を生成します。 メッセージ クラスの概要については、「MAPI メッセージ [クラス」を参照してください](mapi-message-classes.md)。 メッセージ クラスとフォームの詳細については、「 [メッセージ クラスの選択」を参照してください](choosing-a-message-class.md)。
    
4. 必要な MAPI フォーム インターフェイスと、特定のフォーム サーバーが必要とする任意のオプション インターフェイスを実装します。 詳細については、「フォーム サーバー コードの [記述」を参照してください](writing-form-server-code.md)。 
    
5. フォーム オブジェクトとフォームが使用するプロパティとのユーザーのやり取りを処理するユーザー インターフェイス コードを記述します。
    
6. フォームのフォーム構成ファイルの作成。 詳細については、「フォーム構成 [ファイルのファイル形式」を参照してください](file-format-of-form-configuration-files.md)。
    
7. ユーザーのコンピューターにフォームをインストールする。 詳細については、「ライブラリへの [フォームのインストール」を参照してください](installing-a-form-into-a-library.md)。
    
手順 1 ~ 5 を同時に実行する場合は、手順 1 ~ 5 を順に実行する必要があります。 フォーム サーバーを開発するプロセスは、多くのプログラミング プロジェクトと同様に、特に定義されたシーケンスが含まれています。 たとえば、フォーム構成ファイルの作成は上記の 2 番目から最後の手順として表示されますが、フォーム構成ファイルは段階的に作成され、フォーム サーバーに機能を追加するほど完全になります。
  
## <a name="see-also"></a>関連項目



[MAPI の概念](mapi-concepts.md)

