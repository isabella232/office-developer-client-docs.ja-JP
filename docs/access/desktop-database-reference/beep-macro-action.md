---
title: マクロ アクション (デスクトップ データベース参照のアクセス) の音を鳴らす
TOCTitle: Beep macro action
ms:assetid: 5ca1600f-7934-3b3d-19fd-f305cda0e5d8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194572(v=office.15)
ms:contentKeyID: 48545092
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm11853
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 96051d8389f4b8ba7005c75ccdb5e2780ba17138
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721473"
---
# <a name="beep-macro-action"></a>Beep マクロ アクション


**適用されます**Access 2013、Office 2013。

コンピューターのスピーカーからビープ音を鳴らす、**ビープ音が**アクションを使用できます。

## <a name="setting"></a>設定値

**ビープ音を鳴らす**アクション引数はありません。

## <a name="remarks"></a>解説

次のような場合に、**ビープ音を鳴らす**アクションを使用できます。

  - 重要な画面変更があったとき。

  - 不適切なデータがコントロールに入力されたとき。たとえば、テキスト ボックス コントロールに数値データが入力された場合などです。

  - マクロが特定のポイントに達したときや、マクロのアクションが完了したとき。

警告音の周波数と継続時間は、ハードウェアに依存するので、コンピューターの機種によって異なる場合があります。

Visual Basic for Applications (VBA) モジュールで**ビープ音を鳴らす**アクションを実行するには、 **DoCmd**オブジェクトの**Beep**メソッドを使用します。

