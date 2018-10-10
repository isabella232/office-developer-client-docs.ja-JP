---
title: Access でのオートメーションのサポート
TOCTitle: Automation with Microsoft Access
ms:assetid: 39fde349-3ba3-7c7a-3c92-316641dc8712
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192643(v=office.15)
ms:contentKeyID: 48544258
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm13783
f1_categories:
- Office.Version=v15
ms.openlocfilehash: bd0e230d2b4c31d497e913e8e1ccf4d2172402e9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478224"
---
# <a name="automation-with-microsoft-access"></a>Access でのオートメーションのサポート


**適用されます**Access 2013 |。Office 2013

Access はオートメーション (以前の OLE オートメーション) をサポートする COM コンポーネントです。このオートメーションのサポートには 2 つの方法があります。つまり、他の COM コンポーネントのオブジェクトを Access で使用することもできれば、Access のオブジェクトを他の COM コンポーネントで使用することもできます。

**New** キーワードまたは **CreateObject** メソッドを使用すると、コンポーネントの新規インスタンスを作成できます。 **GetObject** メソッドを使用すると、コンポーネントの既存のインスタンスに変数を割り当てることができます。

Access では、コンポーネントのタイプ ライブラリへの参照を設定することで、オートメーションを通じてそのコンポーネントを処理する際のパフォーマンスを向上させることができます。また、Access のオブジェクト ブラウザーでは、他のコンポーネントのタイプ ライブラリのオブジェクトやメソッド、プロパティを表示することができます。

Access のタイプ ライブラリには、Access オブジェクトに関する情報が格納されており、この情報はそのオブジェクトを使用する他のコンポーネントに渡されます。 Microsoft Access[の参照を設定](https://msdn.microsoft.com/library/ff194944\(v=office.15\))することができます、コンポーネントからライブラリを入力し、オブジェクト ブラウザー内のオブジェクトを表示します。

オートメーションを通じて Microsoft Access オブジェクトを処理するには、Microsoft Access の **[Application](https://msdn.microsoft.com/library/ff821758\(v=office.15\))** オブジェクトのインスタンスを作成する必要があります。たとえば、Microsoft Access のフォームまたはレポートに Microsoft Excel のデータを表示するとします。このような場合に Microsoft Excel から Microsoft Access を起動するには、キーワード **New** を使って Microsoft Access の **Application** オブジェクトのインスタンスを作成するという方法があります。他にも、 **CreateObject** メソッドを使って Microsoft Access の **Application** オブジェクトの新規インスタンスを作成する方法や、 **GetObject** メソッドを使って Microsoft Access の既存のインスタンスへのオブジェクト変数を示す方法があります。これらのうち、コンポーネントがどの方法をサポートしているかは、そのコンポーネントのマニュアルで確認してください。

Microsoft Access のインスタンスを開始した後、Microsoft Access のオブジェクトを操作するには、 **[OpenCurrentDatabase](https://msdn.microsoft.com/library/ff837226\(v=office.15\))** または **[NewCurrentDatabase](https://msdn.microsoft.com/library/ff195271\(v=office.15\))** メソッドを使って Microsoft Access ウィンドウにデータベースを開くか、あるいは、 **[OpenAccessProject](https://msdn.microsoft.com/library/ff837249\(v=office.15\))** または **[NewAccessProject](https://msdn.microsoft.com/library/ff835758\(v=office.15\))** メソッドを使って Microsoft Access ウィンドウにプロジェクト (.adp) を開く必要があります。

Dao データ アクセス オブジェクトを使用するための手段として Microsoft Access を開いた場合は、Microsoft Access のウィンドウでデータベースを開く必要があります。 オートメーションの操作中に、Microsoft Office 12.0 Access データベース エンジン オブジェクト ライブラリのオブジェクト ライブラリで、 **[DBEngine](https://msdn.microsoft.com/library/ff821724\(v=office.15\))** オブジェクトのプロパティ、Microsoft Access の**アプリケーション**オブジェクトにアクセスするを使用できます。

