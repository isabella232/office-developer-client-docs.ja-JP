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
localization_priority: Priority
ms.openlocfilehash: 9635cdb2a06f610f42e4aa9fc9f998719aebb986
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296963"
---
# <a name="automation-with-microsoft-access"></a>Microsoft Access によるオートメーション

**適用先:** Access 2013、Office 2013

Access はオートメーション (以前の OLE オートメーション) をサポートする COM コンポーネントです。このオートメーションのサポートには 2 つの方法があります。つまり、他の COM コンポーネントのオブジェクトを Access で使用することもできれば、Access のオブジェクトを他の COM コンポーネントで使用することもできます。

**New** キーワードまたは **CreateObject** メソッドを使用すると、コンポーネントの新規インスタンスを作成できます。 **GetObject** メソッドを使用すると、コンポーネントの既存のインスタンスに変数を割り当てることができます。

Access では、コンポーネントのタイプ ライブラリへの参照を設定することで、オートメーションを通じてそのコンポーネントを処理する際のパフォーマンスを向上させることができます。また、Access のオブジェクト ブラウザーでは、他のコンポーネントのタイプ ライブラリのオブジェクトやメソッド、プロパティを表示することができます。

Microsoft Access タイプ ライブラリでは、Microsoft Access オブジェクトに関する情報が他のコンポーネントに提供されます。 コンポーネントから Microsoft Access タイプ ライブラリへの[参照を設定](https://docs.microsoft.com/office/vba/access/Concepts/Settings/set-references-to-type-libraries)すると、オブジェクト ブラウザーでタイプ ライブラリ内のオブジェクトを表示できます。

オートメーションを通じて Microsoft Access オブジェクトを処理するには、Microsoft Access の **[Application](https://docs.microsoft.com/office/vba/api/Access.Application)** オブジェクトのインスタンスを作成する必要があります。たとえば、Microsoft Access のフォームまたはレポートに Microsoft Excel のデータを表示するとします。このような場合に Microsoft Excel から Microsoft Access を起動するには、キーワード **New** を使って Microsoft Access の **Application** オブジェクトのインスタンスを作成するという方法があります。他にも、 **CreateObject** メソッドを使って Microsoft Access の **Application** オブジェクトの新規インスタンスを作成する方法や、 **GetObject** メソッドを使って Microsoft Access の既存のインスタンスへのオブジェクト変数を示す方法があります。これらのうち、コンポーネントがどの方法をサポートしているかは、そのコンポーネントのマニュアルで確認してください。

Microsoft Access のインスタンスを開始した後、Microsoft Access のオブジェクトを操作するには、**[OpenCurrentDatabase](https://docs.microsoft.com/office/vba/api/Access.Application.OpenCurrentDatabase)** または **[NewCurrentDatabase](https://docs.microsoft.com/office/vba/api/Access.Application.NewCurrentDatabase)** メソッドを使用して Microsoft Access ウィンドウにデータベースを開くか、あるいは、**[OpenAccessProject](https://docs.microsoft.com/office/vba/api/Access.Application.OpenAccessProject)** または **[NewAccessProject](https://docs.microsoft.com/office/vba/api/Access.Application.NewAccessProject)** メソッドを使用して Microsoft Access ウィンドウにプロジェクト (.adp) を開く必要があります。

Microsoft DAO が提供する Data Access Objects を使用する手段としてのみ Microsoft Access を開いている場合は、Microsoft Access ウィンドウでデータベースを開く必要はありません。 オートメーションの操作中に Microsoft Office 12.0 Access データベース エンジン オブジェクト ライブラリのオブジェクトにアクセスするには、Microsoft Access **アプリケーション** オブジェクトの **[ DBEngine](https://docs.microsoft.com/office/vba/api/Access.Application.DBEngine)** プロパティを使用できます。

