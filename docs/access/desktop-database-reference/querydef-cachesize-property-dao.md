---
title: QueryDef.CacheSize プロパティ (DAO)
TOCTitle: CacheSize Property
ms:assetid: a84d990e-8180-daa3-7640-47d2be8fd28b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821397(v=office.15)
ms:contentKeyID: 48546899
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 827e0c751101ca68246278c04a408731b77c36a7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885123"
---
# <a name="querydefcachesize-property-dao"></a>QueryDef.CacheSize プロパティ (DAO)


**適用されます**Access 2013、Office 2013。

ローカル メモリにキャッシュされた ODBC データ ソースから取得したレコード数を設定または取得します。値の取得および設定が可能です。長整数型 ( **Long**) の値を使用します。

## <a name="syntax"></a>構文

*式*です。CacheSize

*式***クエリ定義**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**CacheSize** プロパティの値は、5 ～ 1200 の範囲で、利用可能な空きメモリが許容できる値より大きくならないように設定する必要があります。通常の値は 100 です。0 に設定すると、キャッシュがオフになります。

Microsoft Access データベース エンジンは、キャッシュ範囲内のレコードはキャッシュから要求し、キャッシュ範囲外のレコードはサーバーから要求します。

キャッシュから取得したレコードには、他のユーザーが平行してソース データに加えた変更は反映されていません。

