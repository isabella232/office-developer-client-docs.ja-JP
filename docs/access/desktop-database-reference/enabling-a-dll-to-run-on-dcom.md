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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293547"
---
# <a name="enabling-a-dll-to-run-on-dcom"></a>DCOM で実行する DLL の有効化


**適用先:** Access 2013、Office 2013

次の手順では、ビジネスオブジェクトのダイナミックリンクライブラリで、コンポーネントサービス経由で DCOM と Microsoft インターネットインフォメーションサービス (HTTP) の両方を使用できるようにする方法の概要を説明します。

1.  コンポーネント サービス MMC スナップインに新しい空のパッケージを作成します。 コンポーネント サービス MMC スナップインを使ってパッケージを作成し、このパッケージに DLL を追加します。これにより、DCOM を介して .dll にアクセスできるようになりますが、IIS を介したアクセスはできなくなります (.dll のレジストリを確認すると、 **Inproc** キーが空になっているのがわかります。後で説明するようにアクティブ化属性を設定すると、 **Inproc** キーに値が追加されます)。

2.  パッケージにビジネス オブジェクトをインストールします。 または[RDSServer.DataFactory](datafactory-object-rdsserver.md) オブジェクトをパッケージにインポートします。

3.  Set the Activation attribute for the package to **In the creator's process** (Library application). To make the .dll accessible through DCOM and IIS on the same computer, you must set the component's Activation attribute in the Component Services MMC snap-in. After you set the attribute to **In the creator's process**, you will notice that an **Inproc** server key in the registry has been added that points to a Component Services surrogate .dll.

