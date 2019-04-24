---
title: DBEngine プロパティ (DAO)
TOCTitle: Version Property
ms:assetid: b2807dc1-604f-4423-289a-ff38a3d9f31b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822024(v=office.15)
ms:contentKeyID: 48547171
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052986
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 7e22645127f18ad815c398fd38f9ac4615dfadc9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294191"
---
# <a name="dbengineversion-property-dao"></a>DBEngine プロパティ (DAO)


**適用先:** Access 2013、Office 2013

rreturns 現在使用されている DAO のバージョンを返します。 値の取得のみ可能な文字列型 (**String**) の値です。

## <a name="syntax"></a>構文

*式*。バージョン

*式***DBEngine**オブジェクトを表す変数を取得します。

## <a name="remarks"></a>注釈

戻り値は、"<メジャー>.<マイナー>" の形式で評価結果がバージョン番号になる文字列型 (String) の値です。 For example, "3.0". The product version number consists of the version number (3), a period, and the release number (0).

