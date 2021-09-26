---
title: Microsoft Access によるオートメーション
TOCTitle: Automation with Microsoft Access
description: Microsoft Access は、オートメーション (以前の OLE オートメーション) をサポートする COM コンポーネントです。
ms:assetid: 39fde349-3ba3-7c7a-3c92-316641dc8712
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192643(v=office.15)
ms:contentKeyID: 48544258
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm13783
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: 526887b6d63623174f0bcdffd43d87a17270a1b4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558843"
---
# <a name="automation-with-microsoft-access"></a>Microsoft Access によるオートメーション

**適用先:** Access 2013、Office 2013

Access はオートメーション (以前の OLE オートメーション) をサポートする COM コンポーネントです。このオートメーションのサポートには 2 つの方法があります。つまり、他の COM コンポーネントのオブジェクトを Access で使用することもできれば、Access のオブジェクトを他の COM コンポーネントで使用することもできます。

**New** キーワードまたは **CreateObject** メソッドを使用すると、コンポーネントの新規インスタンスを作成できます。 **GetObject** メソッドを使用すると、コンポーネントの既存のインスタンスに変数を割り当てることができます。

Access では、コンポーネントのタイプ ライブラリへの参照を設定することで、オートメーションを通じてそのコンポーネントを処理する際のパフォーマンスを向上させることができます。また、Access のオブジェクト ブラウザーでは、他のコンポーネントのタイプ ライブラリのオブジェクトやメソッド、プロパティを表示することができます。

Microsoft Access タイプ ライブラリは、Microsoft Access オブジェクトに関する情報を他のコンポーネントに提供します。コンポーネントから Microsoft Access タイプ ライブラリへの[参照を設定](https://docs.microsoft.com/office/vba/access/Concepts/Settings/set-references-to-type-libraries)し、オブジェクト ブラウザーでそのオブジェクトを表示できます。

オートメーションを通じて Microsoft Access オブジェクトを処理するには、Microsoft Access の **[Application](https://docs.microsoft.com/office/vba/api/Access.Application)** オブジェクトのインスタンスを作成する必要があります。たとえば、Microsoft Access のフォームまたはレポートに Microsoft Excel のデータを表示するとします。このような場合に Microsoft Excel から Microsoft Access を起動するには、キーワード **New** を使って Microsoft Access の **Application** オブジェクトのインスタンスを作成するという方法があります。他にも、 **CreateObject** メソッドを使って Microsoft Access の **Application** オブジェクトの新規インスタンスを作成する方法や、 **GetObject** メソッドを使って Microsoft Access の既存のインスタンスへのオブジェクト変数を示す方法があります。これらのうち、コンポーネントがどの方法をサポートしているかは、そのコンポーネントのマニュアルで確認してください。

Microsoft Access のインスタンスを開始した後、Microsoft Access のオブジェクトを操作するには、**[OpenCurrentDatabase](https://docs.microsoft.com/office/vba/api/Access.Application.OpenCurrentDatabase)** または **[NewCurrentDatabase](https://docs.microsoft.com/office/vba/api/Access.Application.NewCurrentDatabase)** メソッドを使用して Microsoft Access ウィンドウにデータベースを開くか、あるいは、**[OpenAccessProject](https://docs.microsoft.com/office/vba/api/Access.Application.OpenAccessProject)** または **[NewAccessProject](https://docs.microsoft.com/office/vba/api/Access.Application.NewAccessProject)** メソッドを使用して Microsoft Access ウィンドウにプロジェクト (.adp) を開く必要があります。

Microsoft DAO が提供する Data Access Objects を使用する手段としてのみ Microsoft Access を開いている場合は、Microsoft Access ウィンドウでデータベースを開く必要はありません。 オートメーションの操作中に Microsoft Office 12.0 Access データベース エンジン オブジェクト ライブラリのオブジェクトにアクセスするには、Microsoft Access **アプリケーション** オブジェクトの **[ DBEngine](https://docs.microsoft.com/office/vba/api/Access.Application.DBEngine)** プロパティを使用できます。

