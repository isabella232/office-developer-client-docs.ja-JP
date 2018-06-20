---
title: InfoPath を自動化する外部のアプリケーションから
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d2248d9-ab20-bcaa-d75b-62876c5e95eb
description: Microsoft InfoPath では、アプリケーションのオブジェクトおよび XDocuments コレクションのメソッドを使用して COM オブジェクトとスクリプトを使用して記述されたコードからのアプリケーションの自動化を提供します。
ms.openlocfilehash: 0e3fcc50ec11f5fc8791d37144767bf0398ccda7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799003"
---
# <a name="automating-infopath-from-an-external-application"></a>InfoPath を自動化する外部のアプリケーションから

Microsoft InfoPath では、**アプリケーション**のオブジェクトおよび**XDocuments**コレクションのメソッドを使用して COM オブジェクトとスクリプトを使用して記述されたコードからのアプリケーションの自動化を提供します。 
  
## <a name="overview-of-the-application-and-xdocument-objects"></a>アプリケーションおよび XDocument オブジェクトの概要

**アプリケーション**オブジェクトには、次のオートメーションに使用されるメソッドが含まれています。 
  
|**メソッド**|**説明**|
|:-----|:-----|
|**CacheSolution** <br/> |調べ、キャッシュにし、必要に応じて、フォーム テンプレートの発行された場所から更新します。  <br/> |
|**Quit** <br/> |Microsoft Office InfoPath アプリケーションを終了します。  <br/> |
|**RegisterSolution** <br/> |指定された Microsoft Office InfoPath フォーム テンプレートをインストールします。  <br/> |
|**UnregisterSolution** <br/> |指定された Microsoft Office InfoPath フォーム テンプレートをアンインストールします。  <br/> |
   
**XDocuments**コレクションには、外部の自動化に使用できる以下の方法が含まれています。 
  
|**メソッド**|**説明**|
|:-----|:-----|
|**Close** メソッド  <br/> |指定された Microsoft Office InfoPath フォームを閉じます。  <br/> |
|**New** メソッド  <br/> |新しい Microsoft Office InfoPath フォームを作成します。  <br/> |
|**NewFromSolution** メソッド  <br/> |指定したフォーム テンプレートに基づいて、新しい Microsoft Office InfoPath フォームを作成します。  <br/> |
|**NewFromSolutionWithData** メソッド  <br/> |指定した XML データとフォーム テンプレートを使用して、新しい Microsoft Office InfoPath フォームを作成します。  <br/> |
|**Open** メソッド  <br/> |指定された Microsoft Office InfoPath フォームを開きます。  <br/> |
   
外部アプリケーションから**アプリケーション**オブジェクトを使用するには、InfoPath アプリケーションを表すオブジェクト変数を作成するのに InfoPath アプリケーション ("InfoPath.Application") の ProgID を持つ、 **CreateObject**関数を使用します。 **XDocuments**コレクションにアクセスし、そのメソッドを使用して開くか、InfoPath フォームを作成し、 **XDocuments**プロパティを使用できます。 次の使用例は、Microsoft Visual Basic 6.0 または Visual Basic for Applications (VBA) プログラミング言語を使用して**アプリケーション**オブジェクトへの参照の作成を示しています。 
  
```vb
Dim objIP As Object 
 
Set objIP = CreateObject("InfoPath.Application") 
 
' Open an existing form 
objIP.XDocuments.Open ("C:\MyFolder\MyForm.xml") 
 
' Create a new form based on a form template 
objIP.XDocuments.NewFromSolution ("C:\MyFolder\MyForm.xsn") 

```

> [!NOTE]
> **CreateObject**関数では、遅延バインディングを使用してオブジェクト変数を作成するため、ステートメントの自動補完は、Visual Basic エディターで利用可能なできません。 正しい呼び出し構文の詳細については上記のテーブルにあるリンクを参照してください。 
  

