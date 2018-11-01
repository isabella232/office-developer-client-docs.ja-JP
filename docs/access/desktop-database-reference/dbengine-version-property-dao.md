---
title: DBEngine.Version プロパティ (DAO)
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
ms.openlocfilehash: 865942cdf4cca81cb0d5348725164a4a75a845fb
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870913"
---
# <a name="dbengineversion-property-dao"></a>DBEngine.Version プロパティ (DAO)


**適用されます**Access 2013、Office 2013。

現在使用中の DAO のバージョンを返します。値の取得のみ可能です。文字列型 ( **String**) の値を使用します。

## <a name="syntax"></a>構文

*式*です。バージョン

*式***DBEngine**オブジェクトを表す変数です。

## <a name="remarks"></a>備考

戻り値は、"<メジャー>.<マイナー>" の形式で評価結果がバージョン番号になる文字列型 (String) の値です。たとえば、"3.0" などです。製品のバージョン番号は、バージョン番号 (3)、ピリオド、およびリリース番号 (0) で構成されます。

