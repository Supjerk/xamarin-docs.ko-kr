---
title: ContentProviders 소개
description: Android 운영 체제 콘텐츠 공급자를 사용 하 여 미디어 파일, 연락처 및 일정 정보 등의 공유 데이터에 대 한 액세스를 용이 하 게 합니다. 이 문서에서는 ContentProvider 클래스를 소개 하 고 사용 하는 방법의 두 가지 예제를 제공 합니다.
ms.prod: xamarin
ms.assetid: 6E1810AA-EB70-9AD0-1B32-D9418908CC97
ms.technology: xamarin-android
author: conceptdev
ms.author: crdun
ms.date: 03/09/2018
ms.openlocfilehash: 4105200c48e41b142fc71e3a524023790b683cdb
ms.sourcegitcommit: e268fd44422d0bbc7c944a678e2cc633a0493122
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50105989"
---
# <a name="intro-to-contentproviders"></a>ContentProviders 소개

_Android 운영 체제 콘텐츠 공급자를 사용 하 여 미디어 파일, 연락처 및 일정 정보 등의 공유 데이터에 대 한 액세스를 용이 하 게 합니다. 이 문서에서는 ContentProvider 클래스를 소개 하 고 사용 하는 방법의 두 가지 예제를 제공 합니다._


## <a name="content-providers-overview"></a>콘텐츠 공급자 개요

A *ContentProvider* 데이터 저장소를 캡슐화 하 고 액세스 하기 위한 API를 제공 합니다. 공급자는 일반적으로 데이터 표시/관리에 대 한 UI도 제공 하는 Android 응용 프로그램의 일부로 존재 합니다. 콘텐츠 공급자를 사용 하는 주요 이점은 다른 응용 프로그램 공급자 클라이언트 개체를 사용 하 여 캡슐화 된 데이터에 쉽게 액세스할 수 있도록 (호출을 *ContentResolver*). 함께 콘텐츠 공급자 및 콘텐츠 확인자를 간단 하 게 빌드하고 사용 하는 데이터 액세스를 위한 일관 된 응용 프로그램 간 API를 제공 합니다. 모든 응용 프로그램을 사용 하도록 선택 `ContentProviders` 내부적으로 데이터를 관리 하 고 다른 응용 프로그램에 노출 합니다.

`ContentProvider` 사용자 지정 검색 제안 제공 하도록 응용 프로그램에 필요 하거나 다른 응용 프로그램을 붙여 응용 프로그램에서 복잡 한 데이터를 복사 하는 기능을 제공 하려는 경우. 이 문서에서는 액세스 구축 하는 방법을 보여 줍니다. `ContentProviders` Xamarin.Android를 사용 하 여 합니다.

이 섹션의 구조는 다음과 같습니다.

- **작동 원리** &ndash; 개요는는 `ContentProvider` 및 작동 하는 방식에 대 한 설계 되었습니다.

- **콘텐츠 공급자를 사용** &ndash; 연락처 목록에 액세스 하는 예제입니다.

- **ContentProvider 사용 하 여 데이터를 공유할** &ndash; 작성 및 사용을 `ContentProvider` 동일한 응용 프로그램입니다.

`ContentProviders` 및 해당 데이터에서 작동 하는 커서는 Listview를 채우는 데 종종 사용 됩니다. 참조 된 [Listview 및 어댑터 가이드](~/android/user-interface/layouts/list-view/index.md) 이러한 클래스를 사용 하는 방법에 대 한 자세한 내용은 합니다.

`ContentProviders` 에 의해 노출 Android (또는 다른 응용 프로그램)는 손쉽게 응용 프로그램에 다른 원본에서 데이터를 포함 합니다. 액세스 및 연락처 목록, 사진 또는 응용 프로그램 내에서 달력 이벤트와 같은 데이터를 제공 하면 하며 사용자가 해당 데이터와 상호 작용할 수 있도록 합니다.

사용자 지정 `ContentProviders` 은 사용자 지정 검색 및 복사/붙여넣기 같은 특수 용도 등 다른 응용 프로그램에서 자신의 앱 내에서 사용 하거나 사용 하기 위해 데이터를 패키지 하는 편리한 방법입니다.

이 섹션의에서 항목에서는 몇 가지 간단한 예제를 작성 및 사용을 제공 `ContentProvider` 코드입니다.



## <a name="related-links"></a>관련 링크

- [ContactsAdapter 데모 (샘플)](https://developer.xamarin.com/samples/monodroid/PlatformFeatures/ContactsAdapterDemo/)
- [SimpleContentProvider (샘플)](https://developer.xamarin.com/samples/monodroid/PlatformFeatures/SimpleContentProvider)
- [콘텐츠 공급자 개발자 가이드](http://developer.android.com/guide/topics/providers/content-providers.html)
- [ContentProvider 클래스 참조](https://developer.xamarin.com/api/type/Android.Content.ContentProvider/)
- [ContentResolver 클래스 참조](https://developer.xamarin.com/api/type/Android.Content.ContentResolver/)
- [ListView 클래스 참조](https://developer.xamarin.com/api/type/Android.Widget.ListView/)
- [CursorAdapter 클래스 참조](https://developer.xamarin.com/api/type/Android.Widget.CursorAdapter/)
- [UriMatcher 클래스 참조](https://developer.xamarin.com/api/type/Android.Content.UriMatcher/)
- [Android.Provider](https://developer.xamarin.com/api/namespace/Android.Provider/)
- [ContactsContract 클래스 참조](https://developer.xamarin.com/api/type/Android.Provider.ContactsContract/)
