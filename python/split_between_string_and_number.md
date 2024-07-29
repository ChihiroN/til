'''
import re

srcs = '80kg 65.5kg 72W 69km 100t'.split()
for src in srcs:
    m = re.match(r'^([\d.]+)(\D+)$', src)
    assert m
    
    value, unit = float(m.group(1)), m.group(2)
    print(
        f'{src} -> "{value}", "{unit}"'
    )
