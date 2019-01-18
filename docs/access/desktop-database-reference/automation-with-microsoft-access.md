---
title: Access でのオートメーションのサポート
TOCTitle: Automation with Microsoft Access
description: Microsoft Access は、OLE オートメーションと呼ばれていたオートメーションをサポートする COM コンポーネントです。
ms:assetid: 39fde349-3ba3-7c7a-3c92-316641dc8712
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192643(v=office.15)
ms:contentKeyID: 48544258
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm13783
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 9635cdb2a06f610f42e4aa9fc9f998719aebb986
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716027"
---
# <a name="automation-with-microsoft-access"></a>Microsoft Access によるオートメーション

**適用されます**Access 2013、Office 2013。

Access はオートメーション (以前の OLE オートメーション) をサポートする COM コンポーネントです。このオートメーションのサポートには 2 つの方法があります。つまり、他の COM コンポーネントのオブジェクトを Access で使用することもできれば、Access のオブジェクトを他の COM コンポーネントで使用することもできます。

**New** キーワードまたは **CreateObject** メソッドを使用すると、コンポーネントの新規インスタンスを作成できます。 **GetObject** メソッドを使用すると、コンポーネントの既存のインスタンスに変数を割り当てることができます。

Access では、コンポーネントのタイプ ライブラリへの参照を設定することで、オートメーションを通じてそのコンポーネントを処理する際のパフォーマンスを向上させることができます。また、Access のオブジェクト ブラウザーでは、他のコンポーネントのタイプ ライブラリのオブジェクトやメソッド、プロパティを表示することができます。

Access のタイプ ライブラリには、Access オブジェクトに関する情報が格納されており、この情報はそのオブジェクトを使用する他のコンポーネントに渡されます。 Microsoft Access[の参照を設定](https://docs.microsoft.com/office/vba/access/Concepts/Settings/set-references-to-type-libraries)することができます、コンポーネントからライブラリを入力し、オブジェクト ブラウザー内のオブジェクトを表示します。

オートメーションを通じて Microsoft Access オブジェクトを処理するには、Microsoft Access の **[Application](https://docs.microsoft.com/office/vba/api/Access.Application)** オブジェクトのインスタンスを作成する必要があります。たとえば、Microsoft Access のフォームまたはレポートに Microsoft Excel のデータを表示するとします。このような場合に Microsoft Excel から Microsoft Access を起動するには、キーワード **New** を使って Microsoft Access の **Application** オブジェクトのインスタンスを作成するという方法があります。他にも、 **CreateObject** メソッドを使って Microsoft Access の **Application** オブジェクトの新規インスタンスを作成する方法や、 **GetObject** メソッドを使って Microsoft Access の既存のインスタンスへのオブジェクト変数を示す方法があります。これらのうち、コンポーネントがどの方法をサポートしているかは、そのコンポーネントのマニュアルで確認してください。

後、Microsoft Access のインスタンスを起動したは、Microsoft Access オブジェクトを制御する場合、開く必要がありますデータベースまたはプロジェクト (.adp) Microsoft Access のウィンドウで、 **[OpenCurrentDatabase](https://docs.microsoft.com/office/vba/api/Access.Application.OpenCurrentDatabase)** または NewCurrentDatabase の**[を使用して](https://docs.microsoft.com/office/vba/api/Access.Application.NewCurrentDatabase)** メソッドのデータベースまたはプロジェクトの**[OpenAccessProject](https://docs.microsoft.com/office/vba/api/Access.Application.OpenAccessProject)** または**[NewAccessProject](https://docs.microsoft.com/office/vba/api/Access.Application.NewAccessProject)** メソッドを使用しています。

Dao データ アクセス オブジェクトを使用するための手段として Microsoft Access を開いた場合、Access ウィンドウにデータベースを開く必要はありません。 オートメーションの操作中に、Microsoft Office 12.0 Access データベース エンジン オブジェクト ライブラリで、 **[DBEngine](https://docs.microsoft.com/office/vba/api/Access.Application.DBEngine)** オブジェクトのプロパティ、Microsoft Access の**アプリケーション**オブジェクトにアクセスするを使用できます。

