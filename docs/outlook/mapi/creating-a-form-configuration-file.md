---
title: フォーム構成ファイルを作成します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aaf3b33d-ad2d-4ef8-847f-1ab1eaf08706
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 9ceb7ad347e73f69eca3463ed2edc4438a45a21f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799860"
---
# <a name="creating-a-form-configuration-file"></a>フォーム構成ファイルを作成します。

  
  
**適用されます**: Outlook 
  
フォーム構成ファイルは、フォーム マネージャーを使用しているとクライアント アプリケーションの両方のフォームに関する情報を提供します。 フォーム構成ファイルには、メッセージング クライアント、フォームによって実装された動詞およびフォームでサポートされているプラットフォームで使用するフォームによって公開されたプロパティを含むフォームの場合、広範な仕様が含まれています。
  
フォーム構成ファイルは、.cfg ファイルの拡張子を持つファイル、Windows の初期化ファイルのような形式には プレーン テキスト ファイル セクションの数とすることをお勧めします。 各セクションは、セクション名を角かっこで囲まれているから始まります。 各セクションには、値およびそのセクションに関連する設定を定義する 1 つまたは複数の行が含まれています。 次の種類のいずれかの値があります。
  
- String
    
- 表示される文字列
    
- プラットフォームの文字列
    
- パス名
    
- 整数型 (Integer)
    
- GUID
    
.Cfg ファイルのセクションの詳細については、[フォーム構成ファイルの形式のファイル](file-format-of-form-configuration-files.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[MAPI フォームのサーバーの開発](developing-mapi-form-servers.md)

