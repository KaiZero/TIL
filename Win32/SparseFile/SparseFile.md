HANDLE h = CreateFileW(
		L"C:\\MySparseFile.t",
		GENERIC_READ | GENERIC_WRITE,
		FILE_SHARE_READ,
		0,
		OPEN_EXISTING,
		0,
		0
	);
파일을 생성 후 핸들을 저장해두고 

// dwReturnedBytes는 반환되는 값 - 다른 옵션에서 많이 쓰임
DeviceIoControl(h, FSCTL_SET_SPARSE, NULL, 0, NULL, 0, &dwReturnedBytes, NULL);
이걸 통해 스파스파일로 변환 (여기서 실패하면 파일 시스템이 지원을 안 할 가능성이 높음)