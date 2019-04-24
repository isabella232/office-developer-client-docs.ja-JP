---
title: Microsoft SDK for Java を使用する
TOCTitle: Using the Microsoft SDK for Java
ms:assetid: 35a1adb2-06d6-ff45-f151-f1f60ff9bfe2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249116(v=office.15)
ms:contentKeyID: 48544152
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d297d019602cef7b6fbc4f5b0125b87ef642213f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305996"
---
# <a name="using-the-microsoft-sdk-for-java"></a>Microsoft SDK for Java の使用


**適用先:** Access 2013、Office 2013

Microsoft SDK for Java は、Microsoft Internet Explorer 環境用の開発キットです。JDK 1.1 および Microsoft Win32 仮想マシン (Microsoft VM) に基づく Java プログラムやアプレットの開発に役立つツール、情報、およびサンプルが提供されています。Microsoft SDK for Java は、Microsoft Visual J++ には含まれていません。

Jactivex.exe ユーティリティは、タイプ ライブラリからクラスを生成しますが、コマンド ラインからのみ実行できます。この機能は、Visual J++ 開発環境には統合されていません。[Java Type Library ウィザード](using-the-java-type-library-wizard.md)で生成されるクラスと異なり、SDK で作成されるクラス ラッパーにステップ インすることができます。そのため、コードでの ADO ラッパー クラスの使用方法をデバッグするときに便利です。

この機能は、ADO タイプ ライブラリを読み取り、アプリケーション内でインスタンス化できるクラスを生成します。 これらのクラスは、次の場所に\\ \<生成さ\>\\れ\\ます。\\windows ディレクトリ Java trustlib msado15.dll。

Microsoft SDK for Java を使用して ADO アプリケーションを Java で作成する方法は、ソース コードから見ると、Java Type Library ウィザードを使用する方法と基本的に同じです。コード例については、「[ADO Java クラス ラッパー](ado-java-class-wrappers.md)」を参照してください。以下の手順で示すように、唯一の大きな違いは、最初にラッパー クラスを生成する方法です。

**Microsoft SDK for Java で ADO プロジェクトを作成するには**

1.  コマンド プロンプトから次のように実行します。Microsoft SDK for Java の Bin ディレクトリを含むようにパスを設定するか、またはその場所からコマンドを実行する必要があります。通常、Microsoft SDK for Java は、Visual Studio と同じ場所にインストールされます。次に示すのは、単一のコマンド ステートメントです。
    
    ```vb 
     
    \<path to DevStudio>\<path to Java SDK>\bin\JactiveX.exe /javatlb "C:\program files\common files\system\ado\msado15.dll" 
    ```

2.  次のコマンドを実行して、生成されたクラスをコンパイルします。/g:t スイッチを指定するとデバッグ シンボルの生成がオンになり, .Java シンボルをトレースできるようになります。リリース ビルドでは、このスイッチを削除します。
    
    ```vb 
     
    jvc /g:t c:\<windows>\Java\trustlib\msado15\*.Java 
    ```

3.  To use these files, open your project in Visual J++. From the **Project** menu, choose **Add To Project**. [**ファイル**] を選択し、すべてのを追加します。trustlib\\msado15.dll directory でプロジェクトに生成された JAVA ファイル。

