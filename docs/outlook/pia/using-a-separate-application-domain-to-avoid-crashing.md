---
title: 異なるアプリケーション ドメインを使用してクラッシュを回避する
TOCTitle: Using a separate application domain to avoid crashing
ms:assetid: 7fc6d1e5-7032-47a9-826f-6b5d3b43fef9
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb623114(v=office.15)
ms:contentKeyID: 55119786
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e2490c15da9c993a1a26b50adeb38207457f8286
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722264"
---
# <a name="using-a-separate-application-domain-to-avoid-crashing"></a>異なるアプリケーション ドメインを使用してクラッシュを回避する

**IDTExtensibility2** インターフェイスを実装するマネージ アドインは、すべて同じ既定のアプリケーション ドメインに読み込まれます。アプリケーション ドメイン内のアドインがクラッシュすると、同じアプリケーション ドメイン内の他のアドインも動作しなくなる可能性があります。

この問題を回避するには、アドイン用の shim を作成し、アドインを専用のアプリケーション ドメインに読み込むことができます。shim は、C++ で作成されたアンマネージ ダイナミック リンク ライブラリです。shim を使用するときは、アドインの代わりに shim を登録します。Outlook が shim を読み込むと、shim が対応するアドインを読み込みます。アドインごとに個別に shim を作成して登録する必要があります。マネージ アドイン用の shim の作成方法については、「[Isolating Office Extensions with the COM Shim Wizard ](https://go.microsoft.com/fwlink/?linkid=89109)」を参照してください。

その他の方法で別のアプリケーション ドメインにアドインを読み込むには、Visual Studio 2010 以降のリリースの Office Developer Tools for Visual Studio で Office 開発ツールを使用してアドインを開発します。 これに該当するバージョンの Office Developer Tools for Visual Studio で開発したアドインは、IDTExtensibility2 インターフェイスを実装しないで、**IStartup** インターフェイスを使用します。 こうしたアドインは、Visual Studio が提供するローダー AddinLoader.dll を使用します。このローダーは、汎用の shim のように動作します。 Outlook は、Visual Studio で作成されたアドインについてレジストリを調べます。 

そうしたアドインを Outlook が検出すると、Outlook は AddinLoader.dll を開始します。これにより、Visual Studio Tools for Office ランタイムが開始され、アプリケーション マニフェストが Visual Studio Tools for Office ランタイムに中継されます。 その後、Visual Studio Tools for Office ランタイムは、該当するアドインを個別のアプリケーション ドメインに読み込みます。 Visual Studio がアドインを読み込む方法の詳細については、「[VSTO アドインのアーキテクチャ](https://msdn.microsoft.com/library/bb386298\(v=office.15\))」を参照してください。

