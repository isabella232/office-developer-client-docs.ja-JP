---
title: Outlook PIA のアーキテクチャ
TOCTitle: Architecture of the Outlook PIA
ms:assetid: 89577d14-e6e2-4270-8e72-b0adba378667
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb646255(v=office.15)
ms:contentKeyID: 55119777
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 3bc4a03d5954e28bc423c835ee582993a9ac9bf1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590857"
---
# <a name="architecture-of-the-outlook-pia"></a>Outlook PIA のアーキテクチャ

Outlook のプライマリ相互運用機能アセンブリ (PIA) は、マネージ コードにおける Outlook オブジェクト モデル対応開発を網羅するサポートを提供します。ただし、オブジェクト ブラウザーで PIA を初めて見たときには、PIA に多くの追加インターフェイスが含まれることと、オブジェクトのすべてのメソッド、プロパティ、およびイベント メンバーが同じオブジェクト インターフェイスで公開されているのではないということに、驚くかもしれません。このセクションの各トピックでは、コードでオブジェクト メンバーにアクセスする方法についてのガイドラインと、オブジェクト、メソッド、プロパティ、およびイベントについての情報を探す場所について説明します。

## <a name="in-this-section"></a>このセクションの内容

|トピック|説明|
|:----|:----------|
|[Outlook PIA とオブジェクト モデルの関係](relating-the-outlook-pia-with-the-object-model.md) |COM ベースの Outlook オブジェクト モデルのオブジェクトおよびメンバーと、PIA のマネージ インターフェイスおよびクラスの対応について説明します。|
|[Outlook PIA でのオブジェクト](objects-in-the-outlook-pia.md) |COM オブジェクトにマップされる一般的な .NET インターフェイス、クラス、およびデリゲートについて、および PIA のオブジェクトにアクセスする方法について説明します。|
|[Outlook PIA でのメソッドとプロパティ](methods-and-properties-in-the-outlook-pia.md) |PIA を使用してマネージ コード内のオブジェクトのメソッドとプロパティにアクセスする方法について説明します。|
|[Outlook PIA でのイベント](events-in-the-outlook-pia.md) |PIA のイベント関連のインターフェイス、デリゲート、およびシンク ヘルパー クラスについて説明します。|

## <a name="see-also"></a>関連項目

- [Outlook PIA を使用するためのセットアップ](setting-up-to-use-the-outlook-pia.md)
- [Outlook PIA を使用してマネージ Outlook アドインを開発する](developing-managed-outlook-add-ins-using-the-outlook-pia.md)
- [操作方法 (Outlook 2013 PIA リファレンス)](how-do-i-outlook-2013-pia-reference.md)

