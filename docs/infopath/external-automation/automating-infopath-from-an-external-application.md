---
title: 外部アプリケーションからの InfoPath の自動化
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 4d2248d9-ab20-bcaa-d75b-62876c5e95eb
description: Microsoft InfoPath は、Application オブジェクトと XDocuments コレクションのメソッドを使用して COM とスクリプトを使用して記述されたコードからアプリケーションの自動化を提供します。
ms.openlocfilehash: 8bd62af41ff4cc11a4768b1a054c2587081e6a53
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552130"
---
# <a name="automating-infopath-from-an-external-application"></a>外部アプリケーションからの InfoPath の自動化

Microsoft InfoPath は **、Application** オブジェクトと **XDocuments** コレクションのメソッドを使用して COM とスクリプトを使用して記述されたコードからアプリケーションの自動化を提供します。 
  
## <a name="overview-of-the-application-and-xdocument-objects"></a>アプリケーションおよび XDocument オブジェクトの概要

**Application** オブジェクトには、オートメーションに使用される次のメソッドが含まれています。 
  
|**メソッド**|**説明**|
|:-----|:-----|
|**CacheSolution** <br/> |キャッシュ内を調べ、必要に応じてフォーム テンプレートの発行場所から更新します。  <br/> |
|**Quit** <br/> |Microsoft Office InfoPath アプリケーションを終了します。  <br/> |
|**RegisterSolution** <br/> |指定された Microsoft Office InfoPath フォーム テンプレートをインストールします。  <br/> |
|**UnregisterSolution** <br/> |指定された Microsoft Office InfoPath フォーム テンプレートをアンインストールします。  <br/> |
   
**XDocuments** コレクションには、外部の自動化に使用できる以下のメソッドが含まれています。 
  
|**メソッド**|**説明**|
|:-----|:-----|
|**Close** メソッド  <br/> |InfoPath フォームで指定Microsoft Officeを閉じます。  <br/> |
|**New** メソッド  <br/> |新しい Microsoft Office InfoPath フォームを作成します。  <br/> |
|**NewFromSolution** メソッド  <br/> |指定したフォーム テンプレートに基づいて、新しい Microsoft Office InfoPath フォームを作成します。  <br/> |
|**NewFromSolutionWithData** メソッド  <br/> |指定した XML データとフォーム テンプレートを使用して、新しい Microsoft Office InfoPath フォームを作成します。  <br/> |
|**Open** メソッド  <br/> |指定された Microsoft Office InfoPath フォームを開きます。  <br/> |
   
外部アプリケーションから **Application** オブジェクトを使用するには、**CreateObject** 関数と InfoPath アプリケーションの ProgID ("InfoPath.Application") を使用して、InfoPath アプリケーションを表すオブジェクト変数を作成します。次に、**XDocuments** プロパティを使用して **XDocuments** コレクションにアクセスし、メソッドを使用して InfoPath フォームを開くか作成します。次の例では、Microsoft Visual Basic 6.0 または Visual Basic for Applications (VBA) プログラミング言語を使用する **Application** オブジェクトへの参照の作成を示します。 
  
```vb
Dim objIP As Object 
 
Set objIP = CreateObject("InfoPath.Application") 
 
' Open an existing form 
objIP.XDocuments.Open ("C:\MyFolder\MyForm.xml") 
 
' Create a new form based on a form template 
objIP.XDocuments.NewFromSolution ("C:\MyFolder\MyForm.xsn") 

```

> [!NOTE]
> **CreateObject** 関数は、遅延バインディングを使用してオブジェクト変数を作成するため、Visual Basic Editor ではステートメントの自動補完を利用できません。正しい呼び出し構文の詳細については、上記の表のリンクを参照してください。 
  

