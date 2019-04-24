---
title: Beep マクロアクション (Access デスクトップデータベースリファレンス)
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296865"
---
# <a name="beep-macro-action"></a>Beep マクロ アクション


**適用先:** Access 2013、Office 2013

"Beep/警告音" アクションを使用すると、スピーカーから警告音を鳴らすことができます。

## <a name="setting"></a>Setting

"Beep/警告音" アクションには、引数はありません。

## <a name="remarks"></a>注釈

"Beep/警告音" アクションは、次のような場合に使用します。

  - 重要な画面変更があったとき。

  - 不適切なデータがコントロールに入力されたとき。たとえば、テキスト ボックス コントロールに数値データが入力された場合などです。

  - マクロが特定のポイントに達したときや、マクロのアクションが完了したとき。

警告音の周波数と継続時間は、ハードウェアに依存するので、コンピューターの機種によって異なる場合があります。

To run the **Beep** action in a Visual Basic for Applications (VBA) module, use the **Beep** method of the **DoCmd** object.

