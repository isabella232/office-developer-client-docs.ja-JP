---
title: DCOM で DLL を実行できるようにする
TOCTitle: Enabling a DLL to Run on DCOM
ms:assetid: b405f767-91f0-c869-d34e-7a953de49106
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249859(v=office.15)
ms:contentKeyID: 48547211
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 750848ce0e787506085899f4717730e1ca0a8f13
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868694"
---
# <a name="enabling-a-dll-to-run-on-dcom"></a>DCOM で DLL を実行できるようにする


**適用されます**Access 2013、Office 2013。

次の手順では、ビジネス オブジェクトのダイナミック リンク ライブラリが、コンポーネント サービスを介して DCOM と Microsoft® インターネット インフォメーション サービス (HTTP) の両方を使用できるようにする方法の概要を示します。

1.  コンポーネント サービス MMC スナップインに新しい空のパッケージを作成します。 コンポーネント サービス MMC スナップインを使ってパッケージを作成し、このパッケージに DLL を追加します。これにより、DCOM を介して .dll にアクセスできるようになりますが、IIS を介したアクセスはできなくなります (.dll のレジストリを確認すると、 **Inproc** キーが空になっているのがわかります。後で説明するようにアクティブ化属性を設定すると、 **Inproc** キーに値が追加されます)。

2.  パッケージにビジネス オブジェクトをインストールします。 または[RDSServer.DataFactory](datafactory-object-rdsserver.md) オブジェクトをパッケージにインポートします。

3.  **作成者のプロセスで**[ライブラリ アプリケーションには、パッケージのアクティブ化属性を設定します。 .Dll ファイルを同じコンピューターで DCOM と IIS を介してアクセスできるようにするためには、コンポーネント サービス MMC スナップインで、コンポーネントのアクティブ化属性を設定する必要があります。 **作成者のプロセス内**に属性を設定した後に、コンポーネント サービスへのポインターがアクティブ化する、**インプロセス**サーバーのレジストリ キーが追加されていることがわかります。

