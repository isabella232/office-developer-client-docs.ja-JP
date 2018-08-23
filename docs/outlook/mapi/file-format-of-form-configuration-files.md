---
title: フォーム構成ファイルの形式
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 86e4ebd9-6df2-4346-9ce9-580f80a83884
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 95add2ca747a267b825648f0de82e8c8a83d3eb7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592256"
---
# <a name="file-format-of-form-configuration-files"></a>フォーム構成ファイルの形式

**適用されます**: Outlook 2013 |Outlook 2016 
  
フォーム構成ファイルは、フォームを定義するのにはフォームの開発者によって作成された形式のファイルです。
  
フォーム構成ファイルが使用されるためフォーム マネージャーがフォームをロードするのには、フォーム構成ファイルを使用して、各フォームを定義しなければなりません。 フォーム構成ファイルには、.cfg ファイル名の拡張子が必要です。 ファイルは、Windows 初期化ファイル (.ini ファイル) の一般的な構文に依存します。 

名前付きのセクションに分かれていて、各セクションには、一連エントリと値にはが含まれています。 次の種類のいずれかの値がある: 文字列、表示される文字列、文字列のプラットフォーム、パス、整数、またはグローバル一意識別子、 **GUID**です。 フォーム構成ファイルは、任意のテキスト エディターまたはテキスト形式で保存できるワード プロセッサで作成できます。
  

