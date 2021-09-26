---
title: Beep マクロ アクション (Access desktop database reference)
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
ms.localizationpriority: medium
ms.openlocfilehash: 9384b4b10b5d370518b760eb1c0f7edf9d162eeb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607130"
---
# <a name="beep-macro-action"></a>Beep マクロ アクション


**適用先**: Access 2013、Office 2013

"Beep/警告音" アクションを使用すると、スピーカーから警告音を鳴らすことができます。

## <a name="setting"></a>設定

"Beep/警告音" アクションには、引数はありません。

## <a name="remarks"></a>注釈

"Beep/警告音" アクションは、次のような場合に使用します。

  - 重要な画面変更があったとき。

  - 不適切なデータがコントロールに入力されたとき。たとえば、テキスト ボックス コントロールに数値データが入力された場合などです。

  - マクロが特定のポイントに達したときや、マクロのアクションが完了したとき。

警告音の周波数と継続時間は、ハードウェアに依存するので、コンピューターの機種によって異なる場合があります。

To run the **Beep** action in a Visual Basic for Applications (VBA) module, use the **Beep** method of the **DoCmd** object.

