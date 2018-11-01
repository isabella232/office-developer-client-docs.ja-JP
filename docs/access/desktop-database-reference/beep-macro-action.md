---
title: マクロ アクション (デスクトップ データベース参照のアクセス) の音を鳴らす
TOCTitle: Beep Macro Action
ms:assetid: 5ca1600f-7934-3b3d-19fd-f305cda0e5d8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194572(v=office.15)
ms:contentKeyID: 48545092
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm11853
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 284be6222d0b81e48a061afd1d87dd32c3985feb
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867581"
---
# <a name="beep-macro-action"></a>"Beep/警告音" マクロ アクション


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

