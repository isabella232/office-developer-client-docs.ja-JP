---
title: スクリプト実行に安全なビジネス オブジェクトとしてマークする
TOCTitle: Marking business objects as safe for scripting
ms:assetid: 8ee49aec-672d-96f7-baa6-9261317a4d90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249630(v=office.15)
ms:contentKeyID: 48546295
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fe5d331b7f3ab4685cb930323076d111a25ec68e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289778"
---
# <a name="marking-business-objects-as-safe-for-scripting"></a>スクリプト実行に安全なビジネス オブジェクトとしてマークする

**適用先:** Access 2013、Office 2013

インターネット環境のセキュリティを確保するには、[RDS.DataSpace](dataspace-object-rds.md) オブジェクトの [CreateObject メソッド (RDS)](createobject-method-rds.md) を使用してインスタンス作成されたすべてのビジネス オブジェクトを、"スクリプトを実行しても安全" だとマークする必要があります。ビジネス オブジェクトを DCOM で使用する前に、システム レジストリの License エリアでそのようにマークされていることを確認する必要があります。

ビジネス オブジェクトを、スクリプトを実行しても安全だと手動でマークするには、次のテキストを含む、拡張子 .reg のテキスト ファイルを作成します。次の 2 つの数値によって、スクリプトを実行しても安全な機能が有効になります。

```vb 
 
[HKEY_CLASSES_ROOT\CLSID\<MyActiveXGUID>\Implemented 
Categories\{7DD95801-9882-11CF-9FA9-00AA006C42C4}] 
[HKEY_CLASSES_ROOT\CLSID\<MyActiveXGUID>\Implemented 
Categories\{7DD95802-9882-11CF-9FA9-00AA006C42C4}] 
```

\< *myactivexguid* \>は、ビジネスオブジェクトの16進数の guid 番号です。 Save it and merge it into your registry by using the Registry Editor or double-clicking the .reg file in Windows Explorer.

Microsoft Visual Basic で作成されたビジネスオブジェクトは、パッケージと展開ウィザードを使用して、自動的に "スクリプトを実行しても安全" とマークできます。 When the wizard asks you to specify safety settings, select **Safe for initialization** and **Safe for scripting**.

アプリケーション セットアップ ウィザードの最後の手順では, .htm ファイルと .cab ファイルが作成されます。これらの 2 つのファイルを目的のコンピューターにコピーし, .htm ファイルをダブルクリックすると、ページを読み込んでサーバーを正しく登録できます。

ビジネスオブジェクトは\\既定で windows system32\\occache ディレクトリにインストールされるため、windows\\system32 ディレクトリに移動し、 **HKEY\_クラス\_のルート\\CLSID\\ **を変更します。\< *myactivexguid*\>\\**InprocServer32**レジストリキーを正しいパスに一致させます。


> [!NOTE]
> [!メモ] 初期化の安全性保持またはスクリプト化の安全性保持としてマークされたビジネス オブジェクトに対しては、ネットワーク上のどのユーザーもインスタンス作成および初期化を実行できます。カスタム ビジネス オブジェクトは、不用意にデザインされたり実装されたりしないようにする必要があります。このようなオブジェクトが、ハッカーがホスト サーバーの重要な領域にアクセスして損害を及ぼすという、セキュリティ上の脅威を招かないよう注意してください。


