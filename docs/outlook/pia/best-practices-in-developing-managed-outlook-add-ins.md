---
title: マネージ Outlook アドインの開発でのベスト プラクティス
TOCTitle: Best practices in developing managed Outlook add-ins
ms:assetid: a03246f6-2ca5-4fcb-8e63-a11cfbc8d9a0
ms:mtpsurl: https://msdn.microsoft.com/library/Bb611563(v=office.15)
ms:contentKeyID: 55119784
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5961c66ccdd2b7d243ecfe32a9efb3ceaf9f12b2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623839"
---
# <a name="best-practices-in-developing-managed-outlook-add-ins"></a>マネージ Outlook アドインの開発でのベスト プラクティス

Outlook の相互運用機能アセンブリを使用すると Outlook と相互運用できるマネージ ソリューションを作成できますが、Outlook は .NET Framework より前から存在しており、Visual Basic for Applications (VBA) や Visual Basic などのアンマネージ言語でのプログラミングをサポートするように設計されています。ここでは、Outlook 用のマネージ アドインを開発するときに注意する必要のある最重要事項について説明します。

- [オブジェクトを系統的に解放する](systematically-releasing-objects.md)
- [異なるアプリケーション ドメインを使用してクラッシュを回避する](using-a-separate-application-domain-to-avoid-crashing.md)
- [Office Developer Tools for Visual Studio で提供される信頼できるアプリケーション オブジェクトを使用する](using-a-trusted-application-object-provided-by-office-developer-tools-for-visual-studio.md)
- [イベント ハンドラーで変数の範囲を適切に設定する](scoping-variables-appropriately-in-event-handlers.md)
- [マネージ Outlook アドインでサポートされないテクノロジを回避する](avoiding-unsupported-technologies-in-managed-outlook-add-ins.md)
- [複数のバージョンの Outlook を使用する場合の遅延バインディングの使用](using-late-binding-if-depending-on-multiple-versions-of-outlook.md)

