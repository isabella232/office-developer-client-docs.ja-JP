---
title: QueryDef.CacheSize プロパティ (DAO)
TOCTitle: CacheSize Property
ms:assetid: a84d990e-8180-daa3-7640-47d2be8fd28b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821397(v=office.15)
ms:contentKeyID: 48546899
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 07ccd63bab2b7303b97063e163ad838ac2d37d44
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558066"
---
# <a name="querydefcachesize-property-dao"></a>QueryDef.CacheSize プロパティ (DAO)


**適用先:** Access 2013、Office 2013

ローカルにキャッシュされる ODBC データ ソースから取得するレコード数を設定または取得します。値の取得および設定が可能です。長整数型 ( **Long**) の値を使用します。

## <a name="syntax"></a>構文

*式* .CacheSize

*式* **QueryDef** オブジェクトを表す変数。

## <a name="remarks"></a>注釈

**CacheSize** プロパティの値は、5 ～ 1200 の範囲で、利用可能な空きメモリが許容できる値より大きくならないように設定する必要があります。通常の値は 100 です。0 に設定すると、キャッシュがオフになります。

Microsoft Access データベース エンジンは、キャッシュ範囲内のレコードはキャッシュから要求し、キャッシュ範囲外のレコードはサーバーから要求します。

キャッシュから取得したレコードには、他のユーザーが平行してソース データに加えた変更は反映されていません。

