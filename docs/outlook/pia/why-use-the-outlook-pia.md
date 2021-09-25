---
title: Outlook PIA を使用する理由
TOCTitle: Why use the Outlook PIA
ms:assetid: 5cc9085e-7c97-4698-8cb9-e33e427c02e7
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb645534(v=office.15)
ms:contentKeyID: 55119773
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d8b17b49d2ad8f2e197196071c31b66189974ff4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590479"
---
# <a name="why-use-the-outlook-pia"></a>Outlook PIA を使用する理由

Outlook 98 以来、Outlook は、Outlook の機能のアプリケーションへの統合、Outlook の拡張、または Outlook の自動化を行うためのオブジェクト モデルを開発者に提供しています。このオブジェクト モデルは、コンポーネント オブジェクト モデル (COM) テクノロジと連携するように設計されています。これまで、Outlook アプリケーションの開発者は、Visual Basic for Applications (VBA) および Visual Basic を使用して COM ソリューションを開発してきました。ただし、VBA を使用して開発された Outlook ソリューションには、特に企業環境において展開に制限があり、展開後のアップデートは困難です。

.NET Framework では、クラス ライブラリの豊富なセットが用意されています。また、VBA と COM アドインの多数の制限を解決するテクノロジもサポートされています。ただし、マネージ アプリケーションで COM オブジェクト モデルに対するプログラムを作成するには、.NET と COM 環境の間のブリッジが必要です。 相互運用機能アセンブリは、このようなブリッジとして機能する COM ラッパーです。 そのため、より多くの Outlook ソリューションが、相互運用機能アセンブリを使用するマネージ アプリケーションとして開発されるようになりました。 相互運用機能アセンブリによって .NET と COM の間の相互運用性を可能にするしくみの詳細については、「[COM と .NET の相互運用性の概要](introduction-to-interoperability-between-com-and-net.md)」を参照してください。

相互運用機能アセンブリは、COM 型を記述し、マネージ コードが COM オブジェクト モデルと対話できるようにします。特定の COM 型を記述する相互運用機能アセンブリは、いくつ存在していてもかまいません。タイプ ライブラリの発行元として、Outlook は、COM ベースのオブジェクト モデルの正式な記述を含むプライマリ相互運用機能アセンブリ (PIA) を提供します。通常は、別のソースからの相互運用機能アセンブリではなく、Outlook PIA の使用が最も適しています。

## <a name="using-visual-studio-and-office-developer-tools-for-visual-studio"></a>Visual Studio および Office Developer Tools for Visual Studio を使用する

開発者は、Visual Studio を使用せずにマネージ Outlook ソリューションを作成することもできますが、Visual Studio を使用すると、Outlook の機能をマネージ コードにより容易に統合することができます。展開が容易なため、COM 開発から .NET 開発に移行すると、アドイン開発者にとってさらに便利になります。設計時に、開発者は Office Developer Tools for Visual Studio を使用して、Outlook オブジェクト モデルおよび .NET Framework の両方にアクセスできるアドインを作成できます。実行時に、Visual Studio の Office 開発ツールは、これらのアドイン用のローダーを提供します。ユーザーが Outlook を起動すると、このローダーが共通言語ランタイム (CLR)、Visual Studio Tools for Office ランタイムを起動し、アドイン アセンブリを読み込みます。アセンブリは、Outlook によって開始されたイベントをキャプチャできます。

Visual Studio 2012 は、既定で Office 2010 のアドイン テンプレートをインストールします。Office Developer Tools for Visual Studio を使用して Outlook 2013 の管理対象のアドインを開発するには、Office 2013 のテンプレートを[ダウンロード](https://aka.ms/officedevtoolsforvs2012)する必要があります。

Office Developer Tools for Visual Studio の詳細については、「[Office ソリューションを開発できるようにコンピューターを構成する](https://docs.microsoft.com/visualstudio/vsto/how-to-configure-a-computer-to-develop-office-solutions?view=vs-2017)」を参照してください。 Outlook 用のマネージ アドインのプログラミングの詳細については、「[VSTO アドインのプログラミングについて](https://docs.microsoft.com/visualstudio/vsto/getting-started-programming-vsto-add-ins?view=vs-2017)」を参照してください。

## <a name="see-also"></a>関連項目

- [Outlook PIA のインストールと参照](installing-and-referencing-the-outlook-pia.md)

