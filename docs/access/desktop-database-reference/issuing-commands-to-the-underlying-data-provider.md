---
title: 基になるデータ プロバイダーへのコマンドの発行
TOCTitle: Issuing commands to the underlying data provider
ms:assetid: 9d8ef3f3-d93c-af67-3114-d2c36c78a802
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249716(v=office.15)
ms:contentKeyID: 48546626
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7d8876b180d668be5734233a33714d7541b9c3d1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291089"
---
# <a name="issuing-commands-to-the-underlying-data-provider"></a>基になるデータ プロバイダーへのコマンドの発行

**適用先:** Access 2013、Office 2013

Any command that does not begin with SHAPE is passed through to the data provider. This is equivalent to issuing a shape command in the form "SHAPE {provider command}". これらのコマンドは、 **Recordset**を生成する必要はあり*ません*。 For instance, "SHAPE {DROP TABLE MyTable} is a perfectly valid shape command, assuming the data provider supports DROP TABLE.

この機能により、通常のプロバイダー コマンドとシェイプ コマンドの両方を、同じ接続とトランザクションで実行できます。

