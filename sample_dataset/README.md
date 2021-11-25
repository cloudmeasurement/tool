# Sample Data set
This directory contains sample data set, in *.csv* format, for the three experiments conducted on the AWS. The details of the data files is as follows:

## File description
**1. us-east-1_AZa.csv:** This file contains sample data for the intra-AZ experiment, where instances were hosted in region us-east-1 (North Virginia), AZ a.

**2. us-east-1_a2b.csv:** This file contains sample data for the inter-AZ experiment, where source instances was hosted in region us-east-1 (North Virginia), AZ a and destination instance was hosted in the same region but in AZ b.

**3. NVirginia_to_Frankfurt.csv:** This file contains sample data for the inter-region experiment, where source instance was hosted in region North Virginia (USA) and the destination instance was hosted in region Frankfurt (Germany).

Each of the three files contains a subset a data set, i.e., 300K pings.

## Data format
The format of each of the three *.csv* files is as folles:

_tx,rx,year,month,date,hour,min,rtt_

where:

tx: Transmit timestamp of the ping

rx: Receive timestamp of the ping

year, month , data, hour, min: This date and time information is extracted from the the "tx" timestamp

Each ping lost does not have an "rx" timestamp. Therefore, for completness, we represent "rx" of lost ping by XXXXXXXXXXXXXXXX and set its rtt to 0.0.
