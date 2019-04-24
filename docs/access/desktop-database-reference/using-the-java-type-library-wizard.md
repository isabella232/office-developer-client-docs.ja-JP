---
title: Java Type Library ウィザードを使用する
TOCTitle: Using the Java Type Library Wizard
ms:assetid: 96af770c-c7c2-c905-3c3e-383a5b99cab2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249670(v=office.15)
ms:contentKeyID: 48546455
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a27491acabd19f688eca4159a36dcfcfc486a026
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312083"
---
# <a name="using-the-java-type-library-wizard"></a>Java タイプ ライブラリ ウィザードの使用


**適用先:** Access 2013、Office 2013

The Java Type Library Wizard is a feature of Visual J++ 1.x, integrated into the **Tools** menu of the development environment. Its purpose is to search a type library and create a Java interface that allows access to COM objects. For Visual J++ 6.0, the Java Type Library Wizard has been replaced with [ADO for Windows Foundation Classes](ado-wfc-programming.md).

Java Type Library ウィザードは、[Microsoft SDK for Java](using-the-microsoft-sdk-for-java.md) に組み込まれているコマンド ライン ツールと同様の結果を生成します。ただし、Microsoft SDK for Java で生成されるクラス ラッパーとは異なり、ウィザードが生成するクラス ラッパーにステップ インすることはできません。

java Type Library ウィザードは、次の場所にクラスを生成\\ \<します\>\\。\\windows ディレクトリ\\Java trustlib msado15.dll。 クラスが生成されるディレクトリにある Summary.txt ファイルでは、生成されたクラス定義を確認できます。

Java Type Library ウィザードは、所定のタイプ ライブラリにある列挙型を INT (整数) 型に変換します。また、タイプ ライブラリの各列挙型に対応するインターフェイスも定義します。ADO 列挙型の値は、次の構文で参照できます。

```vb 
 
msado15.<Enum Name>.<constant Name> 
```

次に示す **Command** オブジェクトの **CommandType** プロパティを設定するコードは、この構文の例を示したものです。

```vb 
 
Cmd1.putCommandType( msado15.CommandTypeEnum.adCmdStoredProc ); 
```

または、Java Type Library ウィザードが生成する列挙型ラッパーから継承することもできます。その場合は、構文から "msado15." を削除できます。ただし、すべての ADO オブジェクトと列挙値の前で msado15.\* をまったく参照しなくて済むようにするには、クラスにおいて、参照している各 Java オブジェクトと列挙型インターフェイスから継承する必要があります。

その他のコード例については、「[ADO Java クラス ラッパー](ado-java-class-wrappers.md)」を参照してください。

**Visual J++ バージョン1から Java Type Library ウィザードを実行するには***

1.  From the **Tools** menu, select **Java Type Library Wizard**.

2.  Select "Microsoft ActiveX Data Objects Library" and click **OK**. この時点で (re) は、ADO \\の trustlib ディレクトリ (既定では、c:\\winnt\\java\\trustlib\\msado15.dll) にファイルを生成します。 If you used the Microsoft SDK for Java to already generate classes for ADO, they will be replaced with those from the Java Type Library Wizard.

3.  To use these files, open your project in Visual J++. From the **Project** menu, choose **Add To Project**. [**ファイル**] を選択し、すべてのを追加します。trustlib ディレクトリで生成\\された JAVA ファイル (既定では\\c\\:\\winnt java\\trustlib msado15.dll) がプロジェクトに生成されます。

