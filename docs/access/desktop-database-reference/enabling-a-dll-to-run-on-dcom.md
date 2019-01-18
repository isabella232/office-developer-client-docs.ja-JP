---
title: DCOM で実行する DLL の有効化
TOCTitle: Enabling a DLL to run on DCOM
ms:assetid: b405f767-91f0-c869-d34e-7a953de49106
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249859(v=office.15)
ms:contentKeyID: 48547211
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b97f4e8050cf293621c7b7fc79437c89171d86fc
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715782"
---
# <a name="enabling-a-dll-to-run-on-dcom"></a>DCOM で実行する DLL の有効化


**適用されます**Access 2013、Office 2013。

次のステップでは、DCOM とコンポーネント サービスを使用して Microsoft インターネット インフォメーション サービス (HTTP) の両方を使用するビジネス オブジェクトのダイナミック リンク ライブラリを有効にする方法を説明します。

1.  コンポーネント サービス MMC スナップインに新しい空のパッケージを作成します。 コンポーネント サービス MMC スナップインを使ってパッケージを作成し、このパッケージに DLL を追加します。これにより、DCOM を介して .dll にアクセスできるようになりますが、IIS を介したアクセスはできなくなります (.dll のレジストリを確認すると、 **Inproc** キーが空になっているのがわかります。後で説明するようにアクティブ化属性を設定すると、 **Inproc** キーに値が追加されます)。

2.  パッケージにビジネス オブジェクトをインストールします。 または[RDSServer.DataFactory](datafactory-object-rdsserver.md) オブジェクトをパッケージにインポートします。

3.  **作成者のプロセスで**[ライブラリ アプリケーションには、パッケージのアクティブ化属性を設定します。 .Dll ファイルを同じコンピューターで DCOM と IIS を介してアクセスできるようにするためには、コンポーネント サービス MMC スナップインで、コンポーネントのアクティブ化属性を設定する必要があります。 **作成者のプロセス内**に属性を設定した後に、コンポーネント サービスへのポインターがアクティブ化する、**インプロセス**サーバーのレジストリ キーが追加されていることがわかります。

