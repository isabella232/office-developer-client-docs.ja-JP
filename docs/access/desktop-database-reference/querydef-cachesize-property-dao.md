---
title: QueryDef プロパティ (DAO)
TOCTitle: CacheSize Property
ms:assetid: a84d990e-8180-daa3-7640-47d2be8fd28b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821397(v=office.15)
ms:contentKeyID: 48546899
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0d826781bd668cff0a61c655e55834512a289c17
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301093"
---
# <a name="querydefcachesize-property-dao"></a>QueryDef プロパティ (DAO)


**適用先:** Access 2013、Office 2013

ローカルにキャッシュされる ODBC データソースから取得したレコード数を設定または取得します。 値の取得と設定が可能な長整数型 (**Long**) の値です。

## <a name="syntax"></a>構文

*式*。CacheSize

*式***QueryDef**オブジェクトを表す変数を取得します。

## <a name="remarks"></a>注釈

**CacheSize** プロパティの値は、5 ～ 1200 の範囲で、利用可能な空きメモリが許容できる値より大きくならないように設定する必要があります。通常の値は 100 です。0 に設定すると、キャッシュがオフになります。

Microsoft Access データベース エンジンは、キャッシュ範囲内のレコードはキャッシュから要求し、キャッシュ範囲外のレコードはサーバーから要求します。

キャッシュから取得したレコードには、他のユーザーが平行してソース データに加えた変更は反映されていません。

