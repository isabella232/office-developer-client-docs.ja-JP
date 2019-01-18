---
title: Prepared プロパティ (ADO)
TOCTitle: Prepared property (ADO)
ms:assetid: 33becda2-faab-5000-8904-6ffd8c5805f2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249105(v=office.15)
ms:contentKeyID: 48544116
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231161
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 9541b2d584728c09ee852f628cdfc35f3d170f04
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718071"
---
# <a name="prepared-property-ado"></a>Prepared プロパティ (ADO)


**適用されます**Access 2013、Office 2013。

コンパイルされたバージョンのコマンドを実行前に保存するかどうかを示します。

## <a name="settings-and-return-values"></a>設定値および戻り値

ブール型 ( **Boolean** ) の値を設定または取得します。 **True** に設定されている場合は、コマンドの準備が必要であることを示します。

## <a name="remarks"></a>解説

**Command** オブジェクトを最初に実行する前に、 [CommandText](commandtext-property-ado.md) プロパティで指定されたクエリの準備済み (コンパイル済み) バージョンをプロバイダーで保存するには、 [Prepared](command-object-ado.md) プロパティを使用します。これによって、コマンドの最初の実行は遅くなることがありますが、プロバイダーでコマンドをコンパイルした後はコンパイル済みのコマンドが使用されるので、パフォーマンスが向上します。

このプロパティが **False** の場合、プロバイダーはコンパイル済みバージョンを作成せずに、直接 **Command** オブジェクトを実行します。

プロバイダーがコマンドの準備をサポートしていない場合、このプロパティを **True** に設定すると、すぐにエラーが返されることがあります。エラーを返さない場合、プロバイダーは単にコマンドの準備の要求を無視し、 **Prepared** プロパティを **False** に設定します。

