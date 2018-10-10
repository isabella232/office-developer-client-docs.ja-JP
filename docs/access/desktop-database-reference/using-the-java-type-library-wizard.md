---
title: Java Type Library ウィザードを使用する
TOCTitle: Using the Java Type Library Wizard
ms:assetid: 96af770c-c7c2-c905-3c3e-383a5b99cab2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249670(v=office.15)
ms:contentKeyID: 48546455
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 931434288cbc14da5d3d9d9d53cd250555c7a767
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479343"
---
# <a name="using-the-java-type-library-wizard"></a>Java Type Library ウィザードを使用する


**適用されます**Access 2013 |。Office 2013

Java タイプ ライブラリ ウィザードでは、機能の Visual J では 1.x では、開発環境の [**ツール**] メニューに統合されています。 その目的は、タイプ ライブラリを検索し、COM オブジェクトへのアクセスを可能にする Java インタ フェースを作成します。 Visual j 6.0 の Java タイプ ライブラリ ウィザードは[Windows Foundation クラスの ADO](ado-wfc-programming.md)を交換済み。

Java Type Library ウィザードは、[Microsoft SDK for Java](using-the-microsoft-sdk-for-java.md) に組み込まれているコマンド ライン ツールと同様の結果を生成します。ただし、Microsoft SDK for Java で生成されるクラス ラッパーとは異なり、ウィザードが生成するクラス ラッパーにステップ インすることはできません。

Java タイプ ライブラリ ウィザードでは、次の場所に、クラスが生成されます: \\ \<windows ディレクトリ\>\\Java\\trustlib\\msado15。 クラスが生成されるディレクトリにある Summary.txt ファイルでは、生成されたクラス定義を確認できます。

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

**Visual J では 1.*x のバージョンの Java タイプ ライブラリ ウィザードを実行するには***

1.  **ツール**] メニューの [ **Java タイプ ライブラリ ウィザード]** を選択します。

2.  [Microsoft ActiveX データ オブジェクト ライブラリ] を選択し、[ **OK**] をクリックします。 ここではこの内のファイルを生成する (re)、 \\ADO の trustlib ディレクトリ (既定では c:\\winnt\\java\\trustlib\\msado15)。 既に ADO のクラスを生成するには、Java の Microsoft SDK を使用する場合、Java タイプ ライブラリ ウィザードからのもので置き換えられます。

3.  これらのファイルを使用するには、プロジェクトを開く、Visual J では。 **[プロジェクト**] メニューから**プロジェクトに追加**を選択します。 **ファイル**を選択しのすべてを追加します。生成された JAVA ファイル、 \\trustlib ディレクトリ (既定では c:\\winnt\\java\\trustlib\\msado15) をプロジェクトにします。

