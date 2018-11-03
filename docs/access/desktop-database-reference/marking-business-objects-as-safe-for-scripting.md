---
title: ビジネス オブジェクトに対してスクリプト作成の安全性を明示する
TOCTitle: Marking Business Objects as Safe for Scripting
ms:assetid: 8ee49aec-672d-96f7-baa6-9261317a4d90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249630(v=office.15)
ms:contentKeyID: 48546295
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f638ae278835841ebf297f2472c04235c6a325b4
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936652"
---
# <a name="marking-business-objects-as-safe-for-scripting"></a>ビジネス オブジェクトに対してスクリプト作成の安全性を明示する


**適用されます**Access 2013、Office 2013。

インターネット環境のセキュリティを確保するには、[RDS.DataSpace](dataspace-object-rds.md) オブジェクトの [CreateObject メソッド (RDS)](createobject-method-rds.md) を使用してインスタンス作成されたすべてのビジネス オブジェクトを、"スクリプトを実行しても安全" だとマークする必要があります。ビジネス オブジェクトを DCOM で使用する前に、システム レジストリの License エリアでそのようにマークされていることを確認する必要があります。

ビジネス オブジェクトを、スクリプトを実行しても安全だと手動でマークするには、次のテキストを含む、拡張子 .reg のテキスト ファイルを作成します。次の 2 つの数値によって、スクリプトを実行しても安全な機能が有効になります。

```vb 
 
[HKEY_CLASSES_ROOT\CLSID\<MyActiveXGUID>\Implemented 
Categories\{7DD95801-9882-11CF-9FA9-00AA006C42C4}] 
[HKEY_CLASSES_ROOT\CLSID\<MyActiveXGUID>\Implemented 
Categories\{7DD95802-9882-11CF-9FA9-00AA006C42C4}] 
```

場所\< *MyActiveXGUID* \>は、ビジネス オブジェクトの GUID の 16 進数です。 保存し、レジストリ エディターを使用するか、Windows エクスプ ローラーで .reg ファイルをダブルクリックすると、レジストリにマージすること。

Microsoft Visual Basic 内に作成されるビジネス オブジェクトは、「スクリプトを実行しても安全」とで自動的にパッケージと展開ウィザードとマークできます。 ファミリー セーフティの設定を指定するウィザードが表示されたら、ときに、**初期化**と**スクリプティングの安全性**を選択します。

アプリケーション セットアップ ウィザードの最後の手順では, .htm ファイルと .cab ファイルが作成されます。これらの 2 つのファイルを目的のコンピューターにコピーし, .htm ファイルをダブルクリックすると、ページを読み込んでサーバーを正しく登録できます。

ビジネス オブジェクトは、Windows にインストールするため\\System32\\既定では、ディレクトリを作成は、Windows に移動\\System32 ディレクトリを変更して、 **HKEY\_クラス\_ルート\\CLSID\\ **\< *MyActiveXGUID*\>\\**InprocServer32**のレジストリ キーに正しいパスと一致します。


> [!NOTE]
> [!メモ] 初期化の安全性保持またはスクリプト化の安全性保持としてマークされたビジネス オブジェクトに対しては、ネットワーク上のどのユーザーもインスタンス作成および初期化を実行できます。カスタム ビジネス オブジェクトは、不用意にデザインされたり実装されたりしないようにする必要があります。このようなオブジェクトが、ハッカーがホスト サーバーの重要な領域にアクセスして損害を及ぼすという、セキュリティ上の脅威を招かないよう注意してください。


